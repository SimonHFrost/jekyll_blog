---
layout: post
title: "Rise of the agentic engineer"
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

Shipping software has fundamentally changed. Agentic engineering is taking over, and software engineer's responsibilities have shifted significantly.

In this blog I'll summarise what Agentic Engineering is, why it's significant, and why it's beneficial for everyone.

## What changed

![What changed](/assets/agentic-engineer/what-changed.png)

In case you didn't hear, LLMs are kind of a big deal. The world is realising software is a perfect candidate for the generative output text LLMs produce. There's a ton of training material from open source repositories, and the output is verifiable - if the app works then you can somewhat verify it's doing a good job.

Recent milestones (in the last 6 months!):

- Terminal-first agentic interfaces like [Claude Code](https://serpsculpt.com/claude-code-usage-statistics/) and [Codex](https://codex.danielvaughan.com/2026/04/09/codex-3-million-users-growth-usage-limits/) went mainstream
- Cursor [hit $2B ARR](https://letsdatascience.com/blog/cursor-hit-2-billion-in-revenue-then-it-told-developers-to-stop-coding) and shipped their own foundation model, [Composer 2](https://siliconangle.com/2026/03/19/vibe-coding-startup-cursor-launches-programming-optimized-composer-2-model/)
- [Opus 4.6](https://techcrunch.com/2026/02/05/anthropic-releases-opus-4-6-with-new-agent-teams/) and [Codex 5.3](https://medium.com/@unicodeveloper/claude-code-vs-codex-vs-opencode-which-ai-coding-agent-is-actually-the-best-in-2026-baa9f6fd5374) got good enough to handle vague input, and more ambitious tasks
- Standards like [MCP](https://daily.dev/blog/mcp-model-context-protocol-why-developers-should-care) and [Skills](https://offthegridxp.substack.com/p/the-genius-of-anthropics-claude-agent-skills-2025) solidified, to provide abstractions that give more leverage when building

## The buzz online

![The buzz online](/assets/agentic-engineer/buzz-online.png)

December 2025 was a turning point where LLMs exceeded junior/mid-level skilled engineers in their ability to deal with ambigious input and take on complex tasks.

- Mat Shumer's ["Something big is happening"](https://shumer.dev/something-big-is-happening) details engineers handing over more responsibility to agents
- Simon Willison on how engineers are [reading less code, and how bottlenecks are shifting](https://simonwillison.net/2026/May/6/vibe-coding-and-agentic-engineering/)
- Peter Steinberger (creator of viral AI project OpenClaw) [coining the term 'agentic engineering'](https://steipete.me/posts/just-talk-to-it)

Individually, each of these is an indicator of the industry shifting quickly. Altogether, it shows a fundamental shift in the future of building software.

## Designing instead of coding

![Designing instead of coding](/assets/agentic-engineer/designing.png)

You don't code by typing any more, you describe the problem. It feels less like engineering and more like managing an employee - you talk about what you want, wait, then give feedback. Think of it as a more mature version of vibe coding.

It's a skill like any other, and you have to learn to use it well. Expect a dip in productivity at first while you figure out how to prompt and configure your tooling. It works best on new or early projects, where there's less complexity and more public training material for the model to draw on.

And this is just the beginning. Today you manage one agent, but the tooling is improving fast, and soon you'll be orchestrating whole engineering teams of them. It has already fundamentally changed the way I work.

## Generalists win this round

![Generalists win this round](/assets/agentic-engineer/generalists.png)

For twenty years, the bottleneck in software was implementation. Specialists won — the person who knew the framework deepest shipped fastest. Now the bottleneck is judgment. What should we build? Does this UX make sense? Is this the right architecture? Coding was always a subset of building, and now the rest of building matters more.

This is the best news a generalist has had in a long time. As a front-end engineer by trade, I spend less time typing components and more time on the parts of the business that actually move the needle - devops, UX, and talking to users.

## What about the slop?!

![What about the slop?!](/assets/agentic-engineer/slop.png)

The principles of writing good code haven't changed, and reviewing it is more important than ever. Every line is a liability, so keep them few, lean on good tests, and you'll still keep bugs out of production. Make it work > make it right > make it efficient.

Slop is a discipline problem, not a tooling problem. Best practices still matter — they're what prevent hard-to-debug production issues and keep your velocity up.

## Cautious optimism

![Cautious optimism](/assets/agentic-engineer/cautious-optimism.png)

Don't believe all the hype. Attention-grabbing headlines usually have monetary motives, like baiting engagement or selling you an online course.

From my experience and what clients tell me, it's feels~ 40% faster. Greenfield work is great - controlling it less yields better results as it picks sensible defaults. Legacy work is also amazing, migrations are way easier and summaries of complex architecture make build faster. It's a genuinely seems like a productivity gain across the board.

## I'm rebranding

![I'm rebranding](/assets/agentic-engineer/rebranding.png)

I'm updating my identity to Full-Stack Agentic Engineer.

I still ship full-stack applications every week. I just don't type the code anymore.

This best describes what I do day to day. And tech has always rewarded keeping up and thinking forward. The last time I saw a shift this big was smartphones; before that, the internet itself.

<img class="business-card" src="/assets/agentic-engineer/business-card.png" alt="Business card">

## Conclusion

![Conclusion](/assets/agentic-engineer/conclusion.png)

In a world increasingly consumed by software, agentic engineering is a shift I'd argue is as big as a shift in the industrial industry. Much like object-oriented programming, it's a higher level of abstraction that frees you to think about bigger problems.

It matters because software isn't the bottleneck anymore. Taste, judgement, and domain knowledge are what's holding you back now.

If you're a startup or founder shipping something interesting and you want to move faster, get in touch — simonhfrost(at)gmail.com.
