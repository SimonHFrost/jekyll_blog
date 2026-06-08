---
layout: post
title: "Thin Client with Expo and Next.js"
draft: true
noindex: true
---

<div style="border: 2px dashed #ED1C24; padding: 12px 16px; margin-bottom: 24px; border-radius: 4px;">
  <strong>🚧 Work in progress</strong> — this is a draft. Rough edges ahead.
</div>

I had an existing web app and wanted to be on the App Store and Play Store without rebuilding everything twice. The plan: a thin native client wrapping the web app, built with Expo (React Native) and Next.js, so I write the product once and minimise the platform-specific work.

The catch is that "minimise work" and "feel native enough to pass Apple review" pull in opposite directions. This is a write-up of how I'm threading that needle, and how agentic engineering changed the way I build it.

## The goal: do less, but feel native

Two non-negotiable criteria drove every decision:

1. **It has to feel native.** First impressions matter, especially on iPhone.
2. **It has to pass Apple review.** A thin wrapper that's "just a website" gets rejected.

That ruled out a lazy webview shell. The native layer has to carry its weight on the parts users actually touch first.

### Native-first auth

I use [Clerk](https://clerk.com/) for authentication, with **Sign in with Apple** on native. That single choice does a lot of heavy lifting for the "feels native" impression — the first thing a new user does is a one-tap Apple login, not a clunky web form. It also keeps Apple happy, since Apple login is effectively required once you offer other social logins.

### Wrapping an existing web app

The core product already exists as a web app. The native client leans on it rather than reimplementing it — but the seams (auth, payments, navigation chrome) are where "thin" stops being acceptable and native has to take over.

### Payments, because they're necessary

Payments aren't optional for this product, and on iOS that means In-App Purchase. More on the pain below — it turned out to be one of the most config-heavy parts of the whole build.

Both auth and payments are **core parts of the app**, not afterthoughts, which means real complexity and real third-party integrations. That's exactly the kind of work that's easy to underestimate in a "thin client."

## Modern software development: building this agentically

I built most of this with agentic engineering — handing goals to coding agents and keeping a tight verification loop around them.

### Integration tests tighten the agentic loop

The single biggest improvement to the loop was writing **integration tests**. Tests give the agent a concrete signal for "did this work?" so it can iterate without me babysitting every step.

The limitation: the test framework's **screenshots don't capture all the state**. A screenshot tells you what's on screen, not what's in memory, the network, or native bridges — so some classes of bug stay invisible to the agent.

### Two platforms is the hard part

Agentic engineering gets genuinely harder when there are **two platforms** (the mobile app and the web app) to keep in sync. The fix that worked: **run both inside the agent**. Letting the LLM actually run the mobile app and the web app — and read their logs — gives it the runtime context it needs to debug across the boundary, instead of guessing from static code.

That's the recurring theme: the more of the running system the agent can observe, the more autonomously it can work.

## My agentic engineering flow

- **Claude Opus is my go-to**, with **Codex as a reviewer.** One model drives, a second set of eyes reviews — cheap insurance against confidently-wrong changes.
- **Permission fatigue** is real. Approving every tool call by hand kills the flow.
- [Auto mode](https://claude.com/blog/auto-mode) helps a lot here — it cuts the approval friction so the agent can actually run. _(RC has been great alongside it, too.)_

## Authentication methods

_TODO: expand — Clerk setup, Apple login on native vs. web, session handling across the wrapper._

## Payments

I **started with RevenueCat (RC)**, but quickly hit the reality that **In-App Purchase was a prerequisite** — RevenueCat sits on top of IAP, it doesn't replace the App Store plumbing.

The honest summary: **a lot of config.** Entitlements, products, sandbox testing, and the back-and-forth between App Store Connect and the SDK ate more time than the feature itself.

_TODO: write up the exact setup and the gotchas._

## Claude, I love you, but you're bringing me down

Building agentically isn't all upside. A few rough patches worth naming:

- **Quality drop on complex tasks.** On harder, multi-step work the output quality can dip — see [claude-code#42796](https://github.com/anthropics/claude-code/issues/42796).
- **Users getting locked out** — [claude-code#44257](https://github.com/anthropics/claude-code/issues/44257).
- **Talking to itself** — the model losing track of who said what, [documented here](https://dwyer.co.za/static/claude-mixes-up-who-said-what-and-thats-not-ok.html).

None of these are dealbreakers, but they're the friction you actually feel day-to-day, and worth going in with eyes open.

## Conclusion

Two things I'm taking away from this build:

- **Context is king.** The more context you give agents — running apps, logs, integration tests — the more they can run autonomously. Almost every improvement to my loop came from feeding the agent more of the live system, not from a cleverer prompt.
- **A lot of "dev ops" still isn't solved by coding agents.** The config-heavy, cross-system, credential-juggling work — App Store setup, payments plumbing, multi-platform glue — is still very much hands-on. Agents accelerate the code; they don't yet carry the operational load.

_TODO: tighten the conclusion once the build settles._
