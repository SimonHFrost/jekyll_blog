---
layout: post
title: "Thin Client with Expo and Next.js"
draft: true
noindex: true
---

<pre style="white-space: pre-wrap; word-break: break-word;">
Thin Client with Expo and Next.js
    Minimise work but support native iphone and android
    Main criteria: Feel native, and pass apple review
        Clerk auth with Apple login for native first impression
        Existing webapp
        Payments because they’re necessary
        Both are a core part of the app - significant complexity, integrations
    Modern software development
        Agentic engineering
        Writing integration tests to improve agentic loop
        Limitation of test framework is screenshot doesn’t capture all state
        Agentic engineering is hard because it’s two platforms, solution: run in agent
        Run mobile app and webapp in LLM to inspect logs
    Agentic Engineering flow
Claude Opus is my go-to, with Codex as reviewer        
Permission fatigue
Auto mode https://claude.com/blog/auto-mode and RC is great
    Authentication methods

One Clerk login, one Convex backend, two surfaces. Clerk handles who you are; Convex handles everything you do — and trusts Clerk by verifying its signed token on every request before a single line of app code runs. The mobile app doesn't rebuild the product; it logs in natively, then hands a fresh token into a WebView of the web app, re-minting it every ~50 seconds. And the whole switch to Clerk shipped without a flag day: it ran beside the old password system as a second trusted issuer, quietly migrating each user the next time they signed in. Nobody was locked out. Nobody noticed.

    Payments
        Initially started with RC but IAP was a prereq
        A lot of config
Claude I love you, but you’re bringing me down

    Quality drop for complex tasks: https://github.com/anthropics/claude-code/issues/42796
Users getting locked out: https://github.com/anthropics/claude-code/issues/44257
Talking to itself https://dwyer.co.za/static/claude-mixes-up-who-said-what-and-thats-not-ok.html    
    Conclusion
        Context is King, The more context you give agents the more they can run autonomously
        A lot of ‘dev ops’ isn’t solved with coding agents
</pre>
