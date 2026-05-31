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
</style>

I still ship full-stack applications every week. I just don't type the code anymore.

## What changed

A few things landed at the same time, and the combination is what broke the dam:

- Cursor hit $1B ARR and shipped their own foundation model, Composer
- Terminal-first agents like Claude Code went mainstream
- Opus 4.5 and Codex 5.3 got good enough to handle vague, ambiguous input — the kind of brief a real client actually gives you
- MCP and Skills made tooling composable

Individually, each was incremental. Together, they crossed a threshold. Mat Shumer wrote "something big is happening" and a lot of us nodded.

Peter Steinberger (Austrian creator of OpenClaw) calls this new way of working agentic engineering, and I think the name is going to stick.

## It feels more like managing than coding

The job now looks like this: I describe what I want, the agent goes off, I review, I give feedback, it iterates. Sometimes I have three or four of them running in parallel git worktrees, each on a different feature.

It's closer to being a tech lead than an IC. You're not writing the code, you're setting the standard for what gets merged.

The weird part is the waiting. The first week I felt guilty about it, like I was slacking. Then I realised the waiting was the work — that's when I'm thinking about the next problem, reviewing the last output, deciding what to ship.

## Generalists win this round

For twenty years, the bottleneck in software was implementation. Specialists won — the person who knew the framework deepest shipped fastest.

The bottleneck is now judgment. What should we build? Does this UX make sense? Is this the right architecture? Coding was always a subset of building, and now the rest of building matters more.

This is the best news a generalist has had in a long time.

## Isn't it all slop?

I get asked this constantly. The honest answer is: it can be, if you let it.

The principles haven't changed since I started writing software. Manage complexity by reducing lines of code. Review every change. Manually test the feature instead of trusting the green checkmark. Harden and clean up before merging.

Slop is a discipline problem, not a tooling problem. Bad engineers were shipping bad code with autocomplete in 2015 too.

## The unlock is real, but overstated

The "you'll 100x your output" crowd is selling courses. The "it's all hype" crowd hasn't tried it properly. Both are wrong.

From my own work and from what clients tell me: at least 40% faster, on real projects, with real deadlines. Sometimes much more on greenfield work, sometimes less on tangled legacy code. It's a real productivity gain, not a revolution and not a fad.

## Why the rebrand

I'm updating my title to Full-Stack Agentic Engineer.

Partly because it's accurate — it describes what I actually do day to day. Partly because working in tech has always meant keeping up, and signalling that you've caught the next wave matters. The last time I saw a shift this big was smartphones. Before that, the internet itself.

I want to be on the side of the people building what comes next, not the side explaining why the old way was fine.

## Conclusion

If you're a founder shipping something interesting and you want to move faster, get in touch — simonhfrost(at)gmail.com.

If you're an engineer still typing every line by hand, try going a full week without doing that. See what happens. I think you'll be surprised which parts of the job you miss, and which parts you don't.
