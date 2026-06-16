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

- Terminal-first agentic interfaces like Claude Code and Codex went mainstream
- Cursor hit $1B ARR and shipped their own foundation model, Composer
https://letsdatascience.com/blog/cursor-hit-2-billion-in-revenue-then-it-told-developers-to-stop-coding
- Opus 4.5 and Codex 5.3 got good enough to handle vague input, and more ambitious tasks
- Standards like MCP and Skills solidified, to provide abstractions that give more leverage when building

## The buzz online

The consensus is that December 2025 was a turning point where LLMs exceeded junior/mid-level skilled engineers in their ability to deal with ambigious input and ability to take on complex tasks.

- Mat Shumer "Something big is happening" blog details engineers handing over more responsibility to agents: https://shumer.dev/something-big-is-happening
- Simon Willison says that engineers are reading less code, and how bottlenecks are shifting: https://simonwillison.net/2026/May/6/vibe-coding-and-agentic-engineering/
- Peter Steinberger (creator of viral AI project OpenClaw) coining the term 'agentic engineering'

Individually, each of these is an indicator of the industry shifting quickly. Together, it shows a fundamental shift in how we build software.

## It's more like designing more than coding

It's a more mature version of vibe coding.

It’s like managing an employee - talk to it about what you want, waiting, and giving feedback
You don’t code by typing any more, you describe the problem
You can start with one agent, but there’s potential for managing whole software engineering teams in the future.
It’s a skill, you need to learn how to use it effectively. There’s a drop in productivity  initially as you learn how to prompt and configure tooling
It’s better with new or early projects - there’s generally less complexity and also better training material publicly available
It has fundamentally changed coding workflows

![Levels](/assets/agentic-engineer/levels.png)

## Generalists win this round

For twenty years, the bottleneck in software was implementation. Specialists won — the person who knew the framework deepest shipped fastest.

The bottleneck is now judgment. What should we build? Does this UX make sense? Is this the right architecture? Coding was always a subset of building, and now the rest of building matters more.

This is the best news a generalist has had in a long time.

## What about the slop?!

The principles of writing good code haven't changed. Reviewing code is now more important than ever. Every line of code is a liability, by reducing lines of code, having good tests. Make it work > make it right > make it efficient.

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

In a word that's increasingly consumed by software, Agentic Engineering is a significant technolgy shift I'd argue is as big as the invention of the the iPhone.

Much like object orientated it's a higher level of abstraction.

It's a fundamental shift for the software engineering industry because software isn't the bottleneck anymore. Taste, judgement, and domain knowledge are most likely holding you back.

If you're a startup or founder shipping something interesting and you want to move faster, get in touch — simonhfrost(at)gmail.com.
