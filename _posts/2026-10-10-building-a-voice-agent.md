---
layout: post
title: "Building a voice agent"
description: "What building a coaching assistant taught me about design, verification, and faster feedback loops with coding agents."
draft: true
noindex: true
---

Are you a software engineer in 2026 if you haven't built a chatbot? This year I worked with a client to build a voice coaching assistant. The project showed me how my process has changed since I started using coding agents: implementation is faster, so design, verification, and feedback loops matter even more.

## Design is more important than ever

A product requirements document (PRD) is a useful way to capture what you want to build and why. Traditionally, it's how teams and stakeholders get on the same page. It also turns out to be a good way to communicate with a coding agent.

There's no single best format. A useful PRD answers a few questions: Who is the user? What problem are they trying to solve? What experience do we want to give them? And what are we assuming will work?

The last question is the one I find most valuable. A PRD is a chance to identify the unknowns before an agent starts building around them. For the coaching assistant, I was worried about latency. If someone had to wait too long for a spoken reply, the conversation would stop feeling like a conversation. We also needed to learn how people wanted to see, correct, and confirm a transcription. Those were product questions, not just implementation details.

## Verification is more important than ever

Coding agents can produce changes quickly. That only helps if you can tell whether those changes improved the product. Without quick, reliable feedback, you end up with a queue of open PRs and a lot of polished-looking slop.

For us, that meant daily TestFlight releases and a simple way to report and track feedback. We wanted the coach to use the app often enough that awkward pauses, confusing transcription states, and unnatural replies surfaced while we could still change them.

We also separated some verification from the app release cycle. The coach's system prompt was loaded through [Langfuse Prompt Management](https://langfuse.com/docs/prompt-management/get-started), so the team could adjust and test the assistant's behaviour without waiting for another build. Langfuse also helped us inspect agent calls when a response didn't behave as expected.

## Make the loop faster

Once we could describe the intended experience and get feedback on it, we could focus on the loop that mattered most: make a change, put it in someone's hands, and see whether a voice conversation felt natural.

The original voice pipeline had three stages: speech-to-text, an LLM response, and text-to-speech. Each stage added a delay, and the pauses between turns felt much longer to a person speaking than they did on an architecture diagram. Keeping the stages separate gave us control over transcription, the model, and the voice, but it also gave us more places to wait and more transitions to tune.

As voice models improved, we explored [OpenAI's Realtime API](https://developers.openai.com/api/docs/models/gpt-realtime), which can take audio input and produce audio output in one conversation. That offered a more natural path for fast back-and-forth speech. The trade-off was less control over each separate stage, so we still had to judge it against the experience we wanted rather than assume a newer API was automatically better.

This was the same design-and-verification loop I've always used, but coding agents let us run it more often. The useful measure wasn't how much code we could produce. It was how quickly we could learn from the person who would actually use the product.

## Conclusion

The rules for building elegant software haven't changed. You still need to understand the user, make sensible trade-offs, and test what you've built. Coding agents make implementation faster, which puts more weight on the quality of your design and feedback. In this project, that meant giving the coach a working voice experience early, listening closely, and making the next iteration better.
