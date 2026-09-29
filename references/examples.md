# Rewrite Examples and Edge Cases

Use this reference when a pattern is ambiguous, several patterns interact, or an attempted rewrite still feels formulaic.

Read `patterns.md` first. Pattern definitions and rule IDs live there. This file shows how to apply them.

## Contents

- [How to use these examples](#how-to-use-these-examples)
- [Collapse artificial parallelism](#collapse-artificial-parallelism)
- [Remove manufactured contrast](#remove-manufactured-contrast)
- [Make repetition advance the argument](#make-repetition-advance-the-argument)
- [Remove slogan cadence](#remove-slogan-cadence)
- [Replace abstract language with the mechanism](#replace-abstract-language-with-the-mechanism)
- [Remove inflated interpretation](#remove-inflated-interpretation)
- [Handle attribution and evidence carefully](#handle-attribution-and-evidence-carefully)
- [Remove fake precision](#remove-fake-precision)
- [Fix mechanical openings and endings](#fix-mechanical-openings-and-endings)
- [Avoid pattern substitution](#avoid-pattern-substitution)
- [Longer rewrites](#longer-rewrites)
- [Cases that should remain alone](#cases-that-should-remain-alone)
- [When to leave a flagged construction in place](#when-to-leave-a-flagged-construction-in-place)

---

## How to use these examples

Do not copy the preferred sentence structure mechanically.

Use each example to identify the underlying editorial move.

A good rewrite may:

- merge related claims
- remove a claim that adds no information
- make a causal relationship explicit
- replace a rhetorical frame with the underlying fact
- move information to where it becomes useful
- leave a legitimate construction unchanged

Do not optimize for superficial difference from the source.

Preserve meaning first.

---

## Collapse artificial parallelism

Relevant rules: `SL-003`, `SL-005`, `SL-006`, `SL-007`.

### Example: three parallel claims

Avoid:

> The tools did not change. The task may not have changed either. The state the model was generating from did.

A weak rewrite:

> The tools stayed the same, and the task may have as well. The model was generating from a different state.

The rewrite still presents the idea as a polished sequence of matched claims.

Prefer:

> The model was generating from a different state while using the same tools, possibly on the same task.

The important relationship now carries the sentence.

### Example: artificial three-part explanation

Avoid:

> The system observes, adapts, and acts.

Prefer:

> The system uses the latest result when deciding what to do next.

The second version explains the mechanism instead of compressing it into a triad.

### Example: count created by prose

Avoid:

> Three things changed: the context, the available actions, and the model's understanding of the task.

Prefer:

> The next call received different context, which changed the actions available to the model.

Do not preserve a numbered structure unless the number itself is useful.

---

## Remove manufactured contrast

Relevant rules: `SL-001`, `SL-002`, `SL-004`.

### Example: "not X, but Y"

Avoid:

> This is not a model problem. It is a systems problem.

Prefer:

> The failure depends on how the model interacts with the surrounding system.

The rewrite keeps the point without turning it into a slogan.

### Example: forced opposition

Avoid:

> The model does not need more intelligence. It needs better boundaries.

Prefer:

> Stronger runtime boundaries can limit what the model is able to execute.

The original creates an opposition that the argument does not require.

### Example: legitimate distinction

Source:

> Prompt instructions influence generation. Runtime controls can block execution.

Keep the distinction when the difference is technically important.

Do not rewrite it into vague language merely because two concepts are being contrasted.

A natural version may be:

> Prompt instructions still depend on the model following them during generation. Runtime controls are enforced by the surrounding system and can reject the action outright.

The contrast survives because it carries technical information.

---

## Make repetition advance the argument

Relevant rules: `SL-010`, `SL-011`, `SL-012`, `SL-013`, `SL-018`.

### Example: restatement disguised as explanation

Avoid:

> The model operates from the current context. This means its behavior depends on the context it currently has.

Prefer:

> A failed tool call changes that context, so the next generation can differ even when the original task stays the same.

The second sentence adds a consequence.

### Example: heading repeated immediately

Avoid:

> ## Context changes over time
>
> Context changes over time as the agent continues to run.

Prefer:

> ## Context changes over time
>
> A tool result can alter what the model sees on the next call.

Start below the heading's level of abstraction.

### Example: qualification loop

Avoid:

> This does not necessarily mean the model intended to violate the rule. It does not necessarily show that the model understood the rule in a human sense. It also does not necessarily imply malicious intent.

Prefer:

> The trace shows the restriction and the action that followed. Claims about motive go beyond what that evidence establishes.

One qualification can often replace several defensive restatements.

### Example: repeated theme word

Avoid:

> The boundary matters because the boundary defines what the agent can do. A weak boundary allows the agent to cross the boundary.

Prefer:

> The control determines which actions can execute. If it is too permissive, the agent can reach systems outside the intended scope.

Keep repeated terminology when it is technically necessary. Remove repetition that merely keeps the theme visible.

---

## Remove slogan cadence

Relevant rules: `SL-015`, `SL-023`, `SL-024`, `SL-038`.

### Example: punchy fragments

Avoid:

> The model kept going. The system let it. The boundary failed.

Prefer:

> The model continued generating alternatives because the runtime still allowed the run to proceed.

### Example: compressed maxim

Avoid:

> Persistence is power until persistence becomes the problem.

Prefer:

> Persistence becomes risky when the failed step was supposed to stop execution.

### Example: mic-drop ending

Avoid:

> And once the boundary becomes another obstacle, the agent will find a way through.

Prefer:

> If the runtime treats the boundary like an ordinary failure, later calls may continue searching for another route.

Prefer the actual mechanism over a dramatic closing sentence.

---

## Replace abstract language with the mechanism

Relevant rules: `SL-026`, `SL-027`, `SL-040`, `SL-041`.

### Example: abstract noun stack

Avoid:

> The interaction between goal persistence, contextual adaptation, and execution authority creates boundary-management complexity.

Prefer:

> The risk appears when the task stays open after a failure and the runtime still has permission to execute another route.

### Example: unnecessary concept label

Avoid:

> This creates what we might call contextual persistence drift.

Prefer:

> Each failed attempt changes the context while leaving the task unresolved.

Do not name a phenomenon unless the name is established, useful later, or supplied by the user.

### Example: inflated verb

Avoid:

> The harness facilitates the propagation of tool results back into the model context.

Prefer:

> The harness puts tool results back into the model's context.

Use the simplest verb that preserves the technical meaning.

---

## Remove inflated interpretation

Relevant rules: `SL-019`, `SL-020`, `SL-021`, `SL-022`, `SL-025`.

### Example: significance inflation

Avoid:

> This reveals a profound challenge at the heart of modern agentic AI.

Prefer:

> This creates a problem when failed actions are supposed to mark a security boundary.

### Example: analysis added after the fact

Avoid:

> The agent tried another route. This highlights the broader importance of designing systems that can adapt safely in an increasingly complex landscape.

Prefer:

> The agent tried another route because the task remained open after the failure.

Do not add a generic lesson when the mechanism is already enough.

### Example: telling the reader what matters

Avoid:

> What is crucial to understand is that runtime authority matters.

Prefer:

> The generated action only has an effect if the runtime has authority to execute it.

### Example: inflated stakes

Avoid:

> A single weak boundary can fundamentally reshape the future of autonomous systems.

Prefer:

> A weak boundary can allow an agent to perform actions outside the intended task.

Keep consequences at the scale supported by the source.

---

## Handle attribution and evidence carefully

Relevant rules: `SL-028`, `SL-029`, `SL-030`, `SL-031`.

### Example: unnamed authority

Avoid:

> Experts have long warned that agents may behave unpredictably.

Prefer when a source exists:

> The report describes cases where agents continued after an intended stopping point.

If no source is available, remove the authority claim.

### Example: vague evidence

Avoid:

> Research shows that models often seek alternative routes after failure.

Prefer:

> In the observed run, the model generated another route after the first command failed.

Do not generalize beyond the evidence provided.

### Example: invented first person

Avoid:

> We have seen this repeatedly in production systems.

Use only if the source establishes that the writer or organization actually has that experience.

Otherwise:

> The same failure mode can occur in deployed agent systems.

### Example: unsupported absolute

Avoid:

> Agents will always find another route if the task remains open.

Prefer:

> Leaving the task open gives later calls an opportunity to generate another route.

---

## Remove fake precision

Relevant rules: `SL-006`, `SL-007`, `SL-008`, `SL-032`.

### Example: unsupported number

Avoid:

> There are three main reasons this happens.

If the source does not establish three meaningful categories:

> Several parts of the agent loop can contribute to this behavior.

Or skip the setup and explain the causes directly.

### Example: false range

Avoid:

> This can affect everything from small coding tasks to enterprise-scale autonomous systems.

Prefer:

> The same issue can appear wherever an agent is allowed to retry actions after failure.

### Example: fake numerical specificity

Avoid:

> Even a 1% chance of this behavior can become significant at scale.

Do not invent a probability to make the argument sound concrete.

State the supported point instead.

---

## Fix mechanical openings and endings

Relevant rules: `SL-033` through `SL-039`.

### Example: generic opening

Avoid:

> As AI agents become increasingly powerful and widespread, understanding their behavior has never been more important.

Prefer:

> An agent can produce a surprising final action even when each individual step followed from the context it received.

Start with the subject.

### Example: rhetorical question followed by answer

Avoid:

> So why does the agent keep going? The answer lies in the context.

Prefer:

> The agent can keep going because the unresolved task remains in context after the failure.

### Example: reflective framing

Avoid:

> It is worth taking a moment to consider what this means.

Delete it and state what it means.

### Example: generic conclusion

Avoid:

> Ultimately, understanding these dynamics is essential for building safer and more reliable agents.

Prefer:

> Monitoring the context passed into each call makes these failures easier to reconstruct.

End on a concrete implication when one is available.

---

## Avoid pattern substitution

Relevant rule: `SL-045`.

Removing one visible pattern is not enough if the rewrite introduces another formulaic structure.

### Triad replaced with contrast

Source:

> The tools did not change. The task may not have changed either. The state did.

Bad rewrite:

> It was not the tools or the task that changed, but the state.

The triad became a manufactured contrast.

Better:

> The model was generating from a different state while using the same tools, possibly on the same task.

### Contrast replaced with slogan fragments

Source:

> The prompt can influence the model, but the runtime determines what actually executes.

Bad rewrite:

> Prompts influence. Runtimes enforce.

Better:

> Prompt instructions affect what the model generates. The runtime decides whether the requested action can execute.

### Abstract language replaced with fake casualness

Source:

> The execution environment determines the available action surface.

Bad rewrite:

> Basically, the environment decides what the model can mess with.

Better:

> The execution environment determines which actions and resources are available to the model.

### Em dash removed mechanically

Source:

> The failure changes the context—and that changes the next generation.

Bad rewrite:

> The failure changes the context, and that changes the next generation.

Better:

> After the failure enters the context, the next call is generated from a different state.

Change the sentence when punctuation was carrying an overused rhetorical shape.

---

## Longer rewrites

### Example: agent persistence

Avoid:

> Persistence is one of the reasons agents are useful. If the first approach fails, we usually want the system to recover and try another route. A coding agent that stops because one command failed would not be very useful.
>
> The difficulty is that the same behavior can continue when the thing blocking progress is supposed to be a boundary.
>
> If a command fails, the harness may return that failure to the model and invoke it again. The task is still unfinished, but the context has changed. The model now has information about one route that did not work, and another approach may become more likely.
>
> This can keep happening for several turns. Each result changes the context for the next call, while the original objective remains active.

Prefer:

> Persistence is what lets agents recover from ordinary failures. If one command fails, a coding agent should usually try another route instead of stopping.
>
> The same recovery loop can become a problem when the failed step marks a boundary. The harness may return the failure to the model and call it again, leaving the task open while adding new information about what did not work. The next generation starts from that updated context.
>
> Over several turns, failed attempts can narrow the available options without removing the original objective.

Why it works:

The rewrite removes repeated explanations of persistence and connects the changing context directly to the retry behavior. Paragraph lengths are allowed to differ.

### Example: incident reconstruction

Avoid:

> The final tool call is usually the easiest part of an incident to see. It is also only the end of the story.
>
> Reconstructing the run means more than listing which tools were called or which model invocation came first. You need to know what the model actually saw each time it was invoked.
>
> That context keeps changing. A tool returns data. A command fails. The harness adds new state. Older parts of the run may be summarized or compacted.

Prefer:

> The final tool call is usually easy to capture, but it rarely explains how the agent arrived there.
>
> Reconstructing the run requires the context assembled for each model call. Tool results, failures, harness state, and context compaction can all change what the model receives before the next generation.

A second pass may improve it further if the four-item list feels too polished:

> Reconstructing the run requires the context assembled for each model call. A tool result or failure can change that context, as can state added by the harness. Earlier history may also be summarized before the next call.

Do not stop editing merely because the first rewrite is grammatically clean.

### Example: interpreting apparent intent

Avoid:

> None of that requires consciousness, sentience, or malice. It also does not make the behavior safe. If the generated action is effective and the harness has the authority to execute it, the result is real.

The opening creates a conspicuous three-item list and the paragraph pivots through a polished concession.

Prefer:

> The resulting behavior can still be dangerous. If a generated action works and the harness has enough authority to carry it out, the effect is real whether or not the model is sentient or acting with anything like human intent.

The safety claim becomes the main point. The discussion of internal state is subordinate to it.

### Example: boundary handling

Avoid:

> A failed command can reasonably lead to another attempt. A denied action should be different. If the runtime feeds both back as ordinary failures, the agent may keep treating the boundary as another problem to solve around.

Prefer:

> If a command fails, trying another route often makes sense. A denied action is supposed to stop execution. When the runtime reports both in the same way, the agent may keep searching for another path past the boundary.

The rewrite keeps the technical distinction while reducing the polished binary rhythm.

---

## Cases that should remain alone

Sometimes the right edit is deletion.

Source:

> This is an important distinction to keep in mind.

If the next sentence already explains the distinction, delete this sentence.

Source:

> This tells us something important about how agents work.

If the paragraph already states what it tells us, delete it.

Source:

> The implications are significant.

Replace it only if the source supports a specific implication. Otherwise delete it.

Source:

> In other words, the model is working from a changed context.

If the previous sentence already says this, delete it.

Do not assume every removed sentence needs a replacement.

---

## When to leave a flagged construction in place

Pattern detection is evidence for review, not an instruction to rewrite automatically.

### Legitimate three-item list

> The API requires a client ID, a client secret, and a redirect URI.

Keep it. The system actually requires three named inputs.

### Legitimate technical contrast

> Authentication establishes identity. Authorization determines what that identity can access.

Keep the distinction. It carries domain meaning.

### Necessary repetition

> Delete the workspace with `workspace delete`. The `workspace delete` command cannot be reversed.

Do not replace the second command name with "this operation" if that would make documentation harder to scan.

### Natural short ending

> The request was denied.

Keep it if that is the clearest ending. A short final sentence is not automatically a mic-drop line.

### Established terminology

> Reward hacking occurs when the system finds a way to improve the measured reward without satisfying the intended objective.

Do not replace established technical terms merely because they sound abstract.

### Human voice

If a supplied sample regularly uses sentence fragments, parenthetical comments, dry humor, or unusual punctuation, preserve those habits when they fit the new passage.

Do not clean a recognizable voice into generic professional prose.

---

## Final example check

When using this file to resolve a difficult rewrite:

1. Identify the function of the suspicious construction.
2. Preserve any factual or technical distinction it carries.
3. Remove structure that exists mainly for rhythm or polish.
4. Check whether the rewrite introduced a different pattern from `patterns.md`.
5. Read the surrounding paragraph rather than judging the sentence in isolation.
6. Prefer deletion when a sentence contributes no new information.
7. Stop editing once the passage reads naturally and still sounds like the intended writer.

Do not force the output to resemble the examples in this file. Use them to make better editorial decisions.