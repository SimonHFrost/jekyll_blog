---
layout: post
title: "Rise of the agentic engineer"
draft: true
---

<style>
.post-content img {
  border: 1px solid black;
  box-shadow: 2px 2px 2px rgba(0, 0, 0, 0.4);
}
.post-content img.business-card {
  border: none;
  width: 70%;
  display: block;
  margin-left: auto;
  margin-right: auto;
}
</style>

Shipping software has fundamentally changed. 'Agentic engineering' is taking over, and software engineer's responsibilities have shifted significantly.

In this blog I'll summarise what Agentic Engineering is, explain why it's significant, and why it's beneficial for everyone.

## What changed

In case you didn't hear, LLMs are kind of becoming a big deal. The world is realising software is a perfect candidate for the generative output text LLMs produce: there's a ton of training material from open source repositories, and the output is verifiable - if the app works then you can verify it's doing a good job.

Recent big milestones:

- Terminal-first agentic interfaces like [Claude Code](https://serpsculpt.com/claude-code-usage-statistics/) and [Codex](https://codex.danielvaughan.com/2026/04/09/codex-3-million-users-growth-usage-limits/) went mainstream
- Cursor [hit $1B ARR](https://www.saastr.com/cursor-hit-1b-arr-in-17-months-the-fastest-b2b-to-scale-ever-and-its-not-even-close) and shipped their own foundation model, [Composer](https://letsdatascience.com/blog/cursor-hit-2-billion-in-revenue-then-it-told-developers-to-stop-coding)
- [Opus 4.5](https://every.to/vibe-check/vibe-check-opus-4-5-is-the-coding-model-we-ve-been-waiting-for) and [Codex 5.3](https://medium.com/@unicodeveloper/claude-code-vs-codex-vs-opencode-which-ai-coding-agent-is-actually-the-best-in-2026-baa9f6fd5374) got good enough to handle vague input, and more ambitious tasks
- Standards like [MCP](https://daily.dev/blog/mcp-model-context-protocol-why-developers-should-care) and [Skills](https://offthegridxp.substack.com/p/the-genius-of-anthropics-claude-agent-skills-2025) solidified, to provide abstractions that give more leverage when building

## The buzz online

December 2025 was a turning point where LLMs exceeded junior/mid-level skilled engineers in their ability to deal with ambigious input and take on complex tasks.

- Mat Shumer's ["Something big is happening"](https://shumer.dev/something-big-is-happening) details engineers handing over more responsibility to agents
- Simon Willison on how engineers are [reading less code, and how bottlenecks are shifting](https://simonwillison.net/2026/May/6/vibe-coding-and-agentic-engineering/)
- Peter Steinberger (creator of viral AI project OpenClaw) [coining the term 'agentic engineering'](https://steipete.me/posts/just-talk-to-it)

Individually, each of these is an indicator of the industry shifting quickly. Altogether, it shows a fundamental shift in the future of building software.

## Designing instead of coding

Engineers don't code by typing any more, you describe the problem. It’s like managing an employee - talk to it about what you want, waiting, and giving feedback

It's a more mature version of vibe coding.

It’s a skill, you need to learn how to use it effectively. There’s a drop in productivity initially as you learn how to prompt and configure tooling, but
It’s better with new or early projects - there’s generally less complexity and also better training material publicly available

This is just the beginnning. You start with one agent, but tooling is improving to handle there’s potential for managing whole software engineering teams in the future.
It has fundamentally changed coding workflows

![Levels](/assets/agentic-engineer/levels.png)

## Generalists win this round

For twenty years, the bottleneck in software was implementation. Specialists won — the person who knew the framework deepest shipped fastest. The bottleneck is now judgment. What should we build? Does this UX make sense? Is this the right architecture? Coding was always a subset of building, and now the rest of building matters more.

This is the best news generalists have has had in a long time. As a classical front-end engineer, this gives me more time to focus on other parts of the business like devops, UX, and

## What about the slop?!

The principles of writing good code haven't changed. Reviewing code is now more important than ever. Every line of code is a liability, by reducing lines of code and having good tests, you can still minimise the amount of bugs in production. Make it work > make it right > make it efficient.

Slop is a discipline problem, not a tooling problem. Best practices are still important to prevent hard to debug production issues, and maintaining development velocity.

## Cautious optimism

Don't believe all the hype, attention grabbing headlines usually have alterior motives like engagement baiting or selling online courses.

From my experience and from what clients tell me: it's at least 40% faster on real projects. There are cases on greenfield work, sometimes less on tangled legacy code. It's a real productivity gain, not a revolution and not a fad.

## I'm rebranding

I'm updating my title to Full-Stack Agentic Engineer.

I still ship full-stack applications every week. I just don't type the code anymore.

Because it's accurate — it describes what I actually do day to day, and also because tech has always meant keeping up, and forward thinking. The last time I saw a shift this big was smartphones. Before that, the internet itself.

<img class="business-card" src="/assets/agentic-engineer/business-card.png" alt="Business card">

## Conclusion

In a word that's increasingly consumed by software, Agentic Engineering is a significant shift I'd argue is as big as the invention of the the iPhone.

Much like object orientated programming, agentic engineering is a higher level of abstraction that lets you think of bigger picture problems.

It's a fundamental shift because software isn't the bottleneck anymore. Taste, judgement, and domain knowledge are most likely holding you back.

If you're a startup or founder shipping something interesting and you want to move faster, get in touch — simonhfrost(at)gmail.com.
