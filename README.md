# Cut the Slop

Cut the Slop is an Agent Skill for writing and rewriting prose that avoids common LLM writing habits while preserving the original meaning, evidence, and voice.

It focuses on patterns that make otherwise competent writing feel generated: repeated rhetorical shapes, manufactured contrasts, unnecessary restatement, abstract filler, slogan-like endings, excessive symmetry, fake precision, and similar habits.

It can work from existing text or guide a new draft from the start.

## What it does

Cut the Slop reviews writing at the sentence, paragraph, section, and document level.

The current pattern library covers **45 recurring writing problems**. These include:

- manufactured contrast (`not X, but Y`, `X isn't the problem. Y is.`)
- negative parallelism (`not faster, not cheaper, just better`)
- mirrored syntax (`X changes the model. Y changes the system.`)
- tidy binaries that oversimplify the point (`either control the model or accept the risk`)
- reflexive triads and tetrads (`fast, flexible, reliable`, `clarity, consistency, precision, control`)
- artificial counting (`there are three reasons` when the material was not naturally organized into three)
- fake structural precision (`the problem has four layers`, `this happens in exactly three stages`)
- false ranges (`from startups to global enterprises`, `from simple tasks to complex systems`)
- over-clean taxonomies that force messy material into neat categories
- semantic restatement (`X happens. This means X is happening.`)
- headings immediately repeated by the opening sentence (`## Context changes` followed by `Context changes during a run.`)
- redundant qualification loops (`this does not necessarily mean...`, repeated several ways)
- thematic keyword saturation (repeating `boundary`, `trust`, `control`, or another theme long after the point is clear)
- synonym rotation (calling the same thing a `control`, `safeguard`, `guardrail`, and `enforcement mechanism` just to avoid repetition)
- repeated sentence cadence (`The model adapts. The system responds. The loop continues.`)
- repeated paragraph architecture (every paragraph following `claim → explanation → takeaway`)
- section-level symmetry (every section having the same length, rhythm, opening, or conclusion)
- brand-message overfitting (restating the same positioning claim in every section)
- significance inflation (`this represents a fundamental shift`, `this changes everything`)
- add-on analysis that contributes no new information (`this highlights the broader importance of...`)
- instructions telling the reader what to value (`what is crucial to understand is...`)
- totalizing statements (`everything depends on this`, `the entire system changes`)
- pseudo-profound compression (`persistence is power until persistence becomes the problem`)
- micro-manifesto language (`the future belongs to systems that...`)
- inflated stakes (`this could redefine the future of AI`)
- abstract noun stacks (`alignment, optimization, execution, governance, and control`)
- unnecessary concept labels (`contextual persistence drift`, `execution authority gap`)
- unnamed authorities (`experts agree`, `researchers have long warned`)
- vague evidentiary claims (`research shows`, `studies suggest`) without an identified basis
- invented first-person experience (`we've seen this repeatedly in production`) when the source never established it
- unsupported absolutes (`agents will always find another route`)
- fake numerical precision (`even a 1% failure rate becomes catastrophic`) when no number was supplied
- generic openings (`in today's rapidly evolving AI landscape...`)
- mechanical signposting (`with that in mind`, `turning now to`, `this brings us to`)
- rhetorical questions immediately answered by the writer (`Why does this happen? The answer is context.`)
- reflective framing (`it is worth taking a moment to consider...`)
- generic conclusions (`ultimately, understanding this is essential`)
- quotable or mic-drop endings (`that is the real risk`, `and that changes everything`)
- chat residue in finished prose (`sure`, `absolutely`, `here's a polished version`)
- model-favored vocabulary clusters (`crucial`, `nuanced`, `robust`, `landscape`, `underscore`, `foster`)
- inflated substitutes for simple verbs (`utilize` instead of `use`, `serves to demonstrate` instead of `shows`)
- em-dash dependence (`the state changed—and that changed everything`)
- unnecessary formatting (constant bolding, excessive headings, decorative lists)
- fake casualness (`Yep, totally`, `super quick`, `here's the thing`)
- pattern substitution, where removing one AI tell introduces another (replacing a triad with `not X but Y`, or replacing formal filler with forced slang)

The Skill does not treat these as banned constructions. A three-item list may be completely natural when there are actually three items. Technical writing may need repeated terminology. A real distinction may require contrast.

The question is whether the structure is carrying information or merely making the prose sound polished.

Cut the Slop also checks across longer documents for problems that are easy to miss sentence by sentence: distant repetition, repeated examples, identical section shapes, recurring conclusions, vocabulary saturation, and paragraphs that keep making the same point in different words.

## The main idea

A lot of "humanizer" prompts operate as word filters. They tell the model to avoid certain vocabulary, punctuation, or phrases.

That catches some surface habits, but many of the strongest writing tells are structural.

For example:

> The tools did not change. The task may not have changed either. The state the model was generating from did.

Changing a few words leaves the underlying three-part construction intact.

A better edit changes the structure:

> The model was generating from a different state while using the same tools, possibly on the same task.

Cut the Slop treats that kind of restructuring as part of the edit.

## Source fidelity

The Skill should not improve prose by inventing material.

Rewrites preserve:

- factual claims
- uncertainty
- attribution
- technical distinctions
- numbers and dates
- the scope of the evidence
- the writer's intended point

It does not add invented quotations, experiences, statistics, examples, or supporting evidence.

If the source says something *may* happen, the rewrite should not quietly turn that into something that *will* happen.

## It is not an AI detector

Cut the Slop does not produce an "AI score" and does not claim that text can be proven human-written from prose style alone.

Its rules are editorial.

The useful question is whether a construction is repetitive, vague, over-engineered, unsupported, or poorly matched to the writer and genre.

That also means a flagged pattern is not automatically wrong. Parallel syntax, repetition, short sentences, technical terminology, and rhetorical devices can all belong in good writing.

The Skill keeps them when they are doing useful work.

## Genre matters

Natural writing depends on where the text will be used.

The Skill includes separate guidance for:

- email
- chat and direct messages
- product and landing-page copy
- documentation
- technical writing
- analysis
- articles and essays
- case studies
- social posts
- executive writing

Technical documentation, for example, may need repeated terminology because consistency prevents ambiguity. A casual message can use fragments that would look strange in a report.

When the user supplies examples of their own writing, those samples take priority over generic style preferences.

## How the Skill is organized

```text
cut-the-slop/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── patterns.md
    ├── genres.md
    ├── examples.md
    └── audit.md
```

### `SKILL.md`

The control plane.

It defines the editing workflow, source-fidelity rules, loading order, output behavior, and the references the agent should consult.

### `references/patterns.md`

The canonical pattern library.

Each pattern has a stable rule ID such as `SL-001`, along with detection guidance, exceptions, decision tests, and examples.

This is the main reference used on every invocation.

### `references/genres.md`

Adjusts editorial decisions to the type of writing being produced.

It also defines how to use human writing samples without turning voice matching into phrase imitation.

### `references/examples.md`

Contains difficult before-and-after cases.

Use it when several patterns interact or when a rewrite is technically correct but still sounds formulaic.

### `references/audit.md`

A document-level review for longer work.

It looks for problems that are hard to spot one sentence at a time, including distant repetition, repeated section structure, recurring cadence, and conclusions that keep restating earlier material.

## Example prompts

You can invoke the Skill with ordinary writing requests:

```text
Rewrite this so it sounds natural without changing the meaning.
```

```text
Remove the AI-writing patterns from this section.
```

```text
Keep the technical meaning, but get rid of the polished LLM cadence.
```

```text
Edit this article in my voice. Use the attached samples as the style reference.
```

```text
Review this draft for repeated claims, fake contrasts, abstract filler, and over-engineered structure.
```

```text
Write this section from my notes and avoid formulaic AI prose from the start.
```

The Skill is designed to return the finished writing rather than narrating every rule it applied, unless the user asks for an audit or explanation.

## Example

Before:

> None of that requires consciousness, sentience, or malice. It also does not make the behavior safe. If the generated action is effective and the harness has the authority to execute it, the result is real.

After:

> The resulting behavior can still be dangerous. If a generated action works and the harness has enough authority to carry it out, the effect is real whether or not the model is sentient or acting with anything like human intent.

The edit removes the conspicuous three-item construction and makes the actual safety claim carry the paragraph.

## Pattern IDs

The pattern library uses stable IDs so the same taxonomy can later support other tools.

Examples:

```text
SL-001  Manufactured contrast
SL-005  Reflexive triad/tetrad
SL-010  Semantic restatement
SL-017  Section-level symmetry
SL-026  Abstract noun stack
SL-031  Unsupported absolute
SL-035  Rhetorical question + immediate answer
SL-038  Quotable/mic-drop ending
SL-042  Em-dash dependence
SL-045  Pattern substitution
```

The IDs make it possible to build a linter or editor around the same rule system without maintaining a separate taxonomy.

## Using it as a ChatGPT Skill

Package the Skill directory as `skill.zip` using the standard Skill packaging tooling, then add the archive through your ChatGPT Skills library.

The packaged Skill should contain `SKILL.md`, `agents/openai.yaml`, and the files under `references/`.

No external service or connector is required for the core writing workflow.

## Design principles

**Meaning comes first.**  
A smoother sentence is not an improvement if it changes the claim.

**Fix the structure that caused the problem.**  
Replacing a suspicious word while preserving the same rhetorical template usually does very little.

**Do not manufacture irregularity.**  
Random fragments, slang, typos, and awkward punctuation are not substitutes for natural prose.

**Keep legitimate repetition.**  
Technical terms, commands, names, and other precision-sensitive language should stay stable when consistency helps the reader.

**Stop editing when the prose works.**  
Repeated rewriting can flatten a writer's voice just as easily as under-editing can leave formulaic patterns behind.

## Planned tooling

The rule IDs are intentionally reusable outside the Skill.

Possible additions include:

- a local prose linter
- editor diagnostics tied to individual rule IDs
- document-level repetition checks
- optional before-and-after explanations
- configurable rule severity
- support for personal writing samples
- evaluation fixtures for testing rewrites across models

The Skill remains useful without those tools.

## Contributing

Pattern additions should describe a recognizable writing failure rather than a single disliked phrase.

A useful rule should explain:

- what to detect
- why the construction may be a problem
- when it should remain untouched
- how to test whether a rewrite is actually better
- examples of weaker and stronger versions

New rules should receive stable `SL-###` identifiers.

Examples should preserve the underlying meaning and should not rely on intentionally bad grammar to make the preferred version look better.

## License

Licensed under the Apache License 2.0.

See `LICENSE` for the full license text.