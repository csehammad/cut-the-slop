```markdown
# Pattern Reference

This file defines the canonical writing-pattern system for Cut the Slop.

Read it whenever the Skill is active.

Use the patterns as diagnostic rules, not as a phrase blacklist.

A phrase is evidence only when its function matches the pattern.

For each possible issue:

1. identify what the sentence is doing
2. check whether the structure is required by the information
3. check whether removing the structure improves clarity
4. preserve legitimate factual, logical, technical, or stylistic distinctions
5. revise the underlying structure rather than swapping surface vocabulary

## Contents

### Contrast, symmetry, and artificial structure

- SL-001 Manufactured contrast
- SL-002 Negative parallelism
- SL-003 Mirrored syntax
- SL-004 Tidy binary
- SL-005 Reflexive triad or tetrad
- SL-006 Artificial counting
- SL-007 Fake structural precision
- SL-008 False range
- SL-009 Over-clean taxonomy

### Progression and repetition

- SL-010 Semantic restatement
- SL-011 Restated heading
- SL-012 Redundant qualification
- SL-013 Thematic keyword saturation
- SL-014 Synonym rotation
- SL-015 Repeated cadence
- SL-016 Repeated paragraph architecture
- SL-017 Section-level symmetry
- SL-018 Brand-message overfitting

### Inflation and abstraction

- SL-019 Significance inflation
- SL-020 Add-on analysis
- SL-021 Reader-value instruction
- SL-022 Totalizing statement
- SL-023 Pseudo-profound compression
- SL-024 Micro-manifesto language
- SL-025 Inflated stakes
- SL-026 Abstract noun stack
- SL-027 Concept labeling

### Evidence, attribution, and scope

- SL-028 Unnamed authority
- SL-029 Vague evidentiary coverage
- SL-030 Invented first-person experience
- SL-031 Unsupported absolute
- SL-032 Fake precision

### Openings, transitions, and endings

- SL-033 Generic opener
- SL-034 Mechanical signposting
- SL-035 Rhetorical question with immediate answer
- SL-036 Reflective framing
- SL-037 Generic conclusion
- SL-038 Quotable or mic-drop ending
- SL-039 Chat residue

### Vocabulary, formatting, and surface habits

- SL-040 Model-favored vocabulary cluster
- SL-041 Inflated substitute for a simple verb
- SL-042 Em-dash dependence
- SL-043 Unnecessary formatting
- SL-044 Fake casualness
- SL-045 Pattern substitution

---

# Contrast, symmetry, and artificial structure

## SL-001 Manufactured contrast

### Detect

Flag a sentence when it creates an opposition that the underlying information does not require.

Common forms:

- not X, but Y
- not just X, but Y
- it is not about X; it is about Y
- X is not merely A. It is B.
- X does this. Y does that.
- less about X, more about Y

### Decision test

Ask whether X and Y actually conflict, exclude one another, or need comparison.

If they can simply coexist, state the useful relationship directly.

### Do not flag

Preserve real distinctions, corrections, exclusions, or mutually exclusive states.

Technical example:

> The API does not delete the record. It marks it inactive.

The contrast conveys actual system behavior.

### Avoid

> The tool is not just about automation. It is about giving teams control.

### Prefer

> The tool automates routine work and gives teams controls for reviewing exceptions.

---

## SL-002 Negative parallelism

### Detect

Flag repeated sentence structures that define an idea through negation before stating it positively.

Common forms:

- not X, but Y
- not A. Not B. C.
- it isn't X. It isn't Y. It is Z.
- no X, no Y, just Z

This pattern often creates drama without adding information.

### Decision test

Ask whether the negative clauses rule out realistic interpretations the reader might otherwise have.

If not, state the positive claim directly.

### Do not flag

Keep negation when correcting a likely misunderstanding or specifying an important boundary.

### Avoid

> This is not a reporting problem. It is not a tooling problem. It is a process problem.

### Prefer

> The delays come from the approval process.

---

## SL-003 Mirrored syntax

### Detect

Flag adjacent claims that use deliberately balanced grammar even though the content does not require balance.

Examples:

- X handles A; Y handles B.
- one side does X, the other does Y
- where X brings A, Y brings B
- the system provides speed; the team provides judgment

### Decision test

Ask whether the parallel form clarifies a genuine comparison.

If the symmetry exists mainly for cadence, rewrite around the actual relationship.

### Do not flag

Parallel syntax is useful in genuine comparisons, specifications, contracts, and tables.

### Avoid

> Automation brings speed. Human review brings judgment.

### Prefer

> Automation processes routine cases quickly, while reviewers handle cases that require interpretation.

---

## SL-004 Tidy binary

### Detect

Flag explanations that reduce a complex issue to two clean sides without evidence that the issue has only two relevant dimensions.

Common forms:

- speed versus quality
- automation versus judgment
- efficiency versus control
- humans versus machines
- strategy versus execution

### Decision test

Ask whether the source establishes two distinct competing factors.

If the division is rhetorical convenience, remove it.

### Do not flag

Use binaries when the underlying system genuinely has two states, options, categories, or competing constraints.

### Avoid

> The challenge is simple: move fast or maintain quality.

### Prefer

> Faster review times can increase error rates when staffing and validation stay unchanged.

---

## SL-005 Reflexive triad or tetrad

### Detect

Flag groups of three or four when the number appears chosen for rhythm rather than because the material naturally contains that many items.

Typical forms:

- faster, smarter, safer
- clarity, consistency, control
- plan, build, launch
- simple, scalable, secure, reliable

### Decision test

Ask whether every item contributes a distinct necessary idea.

If one item is weak, overlapping, or decorative, remove it.

### Do not flag

Keep real sets such as three required steps, four supported formats, or three independently meaningful findings.

### Avoid

> The platform is faster, smarter, and more reliable.

### Prefer

> The platform reduced processing time in the benchmark provided.

---

## SL-006 Artificial counting

### Detect

Flag announced counts that exist mainly to package an argument.

Common forms:

- three things matter
- there are two reasons
- one problem, three consequences
- four lessons stand out

### Decision test

Ask whether knowing the number helps the reader navigate or remember genuinely separate items.

If the count adds no value, remove the announcement.

### Do not flag

Keep numbered procedures, requirements, ranked criteria, contractual conditions, and other genuinely countable structures.

### Avoid

> Three things make this approach different.

### Prefer

> The approach uses local processing and keeps the source text available during revision.

---

## SL-007 Fake structural precision

### Detect

Flag precise-looking counts, stages, layers, pillars, dimensions, or phases that were invented to make the explanation appear systematic.

Examples:

- the five pillars of...
- a three-layer framework
- four dimensions define...
- the two-part problem

### Decision test

Ask where the structure came from.

If it was not supplied by the source, derived from a real process, or genuinely useful to the explanation, do not invent it.

### Do not flag

Keep explicit frameworks, documented stages, real system layers, and user-requested categorizations.

### Avoid

> The problem has three layers: content, structure, and perception.

### Prefer

> The draft repeats ideas, relies on symmetrical phrasing, and makes claims the source does not support.

---

## SL-008 False range

### Detect

Flag "from X to Y" constructions when X and Y do not define a meaningful spectrum, sequence, or scope.

Examples:

- from strategy to execution
- from insight to impact
- from idea to outcome
- from complexity to clarity

### Decision test

Ask whether intermediate points between X and Y have a meaningful relationship.

If not, list or describe the actual scope.

### Do not flag

Keep real numeric, geographic, temporal, procedural, or ordinal ranges.

### Avoid

> The product supports teams from ideation to execution.

### Prefer

> The product supports planning, drafting, review, and publishing workflows.

---

## SL-009 Over-clean taxonomy

### Detect

Flag explanations that divide messy material into unusually neat, equally weighted categories.

Signals:

- every section has the same number of items
- categories overlap
- exceptions are ignored
- category names sound designed before the evidence was examined

### Decision test

Ask whether each category is independently useful and supported.

Allow categories to differ in size and importance.

### Do not flag

Keep established taxonomies or classifications required by the domain.

### Avoid

> Every writing problem falls into one of four buckets: structure, tone, clarity, or trust.

### Prefer

> Common problems include repeated claims, unsupported specifics, rigid structure, and inflated language. Some passages exhibit several at once.

---

# Progression and repetition

## SL-010 Semantic restatement

### Detect

Flag a sentence that repeats an earlier claim without adding a fact, reason, mechanism, consequence, example, or qualification.

Compare meaning rather than exact words.

### Decision test

Ask:

> What does the reader know after this sentence that they did not know before it?

If the answer is nothing, delete or replace it.

### Do not flag

Intentional repetition may be appropriate in instructions, legal language, speeches, or when the user explicitly wants emphasis.

### Avoid

> Reviewers make the final decision. Final approval remains with the reviewer.

### Prefer

> Reviewers make the final decision.

---

## SL-011 Restated heading

### Detect

Flag an opening sentence that merely converts the section heading into prose.

### Decision test

Remove the first sentence mentally.

If the section becomes stronger and loses no information, delete it.

### Do not flag

A short orienting sentence can remain when it adds necessary scope or context.

### Avoid

#### Review process

> The review process determines how work is reviewed.

### Prefer

#### Review process

> Requests above the approval threshold are routed to a senior reviewer.

---

## SL-012 Redundant qualification

### Detect

Flag repeated cautionary language after the scope has already been established.

Examples:

- may potentially
- could possibly
- in some cases may
- depending on the circumstances, it may sometimes
- generally tends to

Also flag the same caveat repeated across several sentences.

### Decision test

Choose the correct degree of certainty once.

### Do not flag

Keep separate qualifications when they apply to different claims.

### Avoid

> The change may potentially reduce delays in some cases, depending on how teams use it.

### Prefer

> The change may reduce delays when teams use the new approval path.

---

## SL-013 Thematic keyword saturation

### Detect

Flag repeated use of the same thematic or brand word beyond what precision requires.

Examples:

- trust repeated in every paragraph
- judgment repeated across every section
- control repeated in headings and conclusions
- clarity repeated as a generic virtue

### Decision test

Ask whether each occurrence identifies something concrete.

If the word mainly reinforces a theme, cut some instances.

### Do not flag

Repeat technical terms when synonym replacement would reduce precision.

### Avoid

> Trust starts with transparent controls. Trust also depends on review. These trust mechanisms help teams build trust at scale.

### Prefer

> Transparent controls show who approved a change and when. Reviewers can inspect the same record later.

---

## SL-014 Synonym rotation

### Detect

Flag consecutive substitutions made only to avoid repeating a precise term.

Examples:

- user → customer → individual → person
- reviewer → approver → evaluator → assessor
- system → platform → solution → technology

### Decision test

If all words refer to the same entity, prefer consistent terminology.

### Do not flag

Use different terms when they identify genuinely different concepts.

### Avoid

> The reviewer checks the request. The evaluator then records a decision. The assessor can add notes.

### Prefer

> The reviewer checks the request, records a decision, and can add notes.

---

## SL-015 Repeated cadence

### Detect

Flag several nearby sentences built with the same rhythmic template.

Examples:

- short declaration + explanation
- short declaration + explanation
- short declaration + explanation

Or:

- 8-word sentence
- 15-word sentence
- 5-word punchline
- repeated again

### Decision test

Read the passage for rhythm independently of meaning.

If the cadence becomes predictable, restructure one or more sentences.

### Do not flag

Repetition can aid comprehension in procedures or deliberate rhetorical writing.

### Avoid

> The process is simple. Teams submit a request through the form.  
> The review is fast. Approvers receive the request immediately.  
> The result is clear. Everyone sees the final status.

### Prefer

> Teams submit requests through the form. Approvers receive them immediately, and the final status remains visible to everyone involved.

---

## SL-016 Repeated paragraph architecture

### Detect

Flag several paragraphs that perform the same rhetorical sequence.

Example template:

1. opening claim
2. explanation
3. example
4. punchline

### Decision test

Label the function of each sentence in consecutive paragraphs.

If the labels repeat mechanically, change the structure where the content allows.

### Do not flag

Repeated structure is appropriate for reference documentation, catalogs, specifications, and standardized reports.

### Avoid

Every product section follows:

> Feature claim → explanation → benefit → slogan.

### Prefer

Let each section use the structure its information requires.

---

## SL-017 Section-level symmetry

### Detect

Flag documents in which sections have suspiciously similar length, syntax, heading style, number of bullets, and conclusions.

### Decision test

Ask whether the subject matter is actually equally complex.

If one section needs two paragraphs and another needs six, allow the difference.

### Do not flag

Use consistent section templates where comparability is the purpose, such as product comparisons or recurring reports.

### Avoid

Every section contains exactly:

- two paragraphs
- three bullets
- one closing takeaway

### Prefer

Give each section enough space for its actual content.

---

## SL-018 Brand-message overfitting

### Detect

Flag repeated attempts to reconnect every feature, paragraph, or section to the same positioning statement.

### Decision test

Ask whether the reader already understands the brand claim.

If so, explain the feature or evidence directly.

### Do not flag

Brand repetition may be appropriate in short advertising formats where repetition is intentional.

### Avoid

> The approval log gives teams control.  
> Export settings give teams control.  
> Role permissions give teams control.

### Prefer

> The approval log records decisions. Export settings determine what leaves the system, and role permissions restrict who can change configuration.

---

# Inflation and abstraction

## SL-019 Significance inflation

### Detect

Flag language that announces importance instead of demonstrating it.

Signals:

- crucial
- vital
- transformative
- groundbreaking
- defining
- pivotal
- profound
- game-changing
- significant when no significance is established

### Decision test

Replace the importance claim with the actual consequence.

If there is no concrete consequence, remove the emphasis.

### Do not flag

Keep evaluative language when evidence or the requested genre supports it.

### Avoid

> This marks a transformative shift in how teams approach governance.

### Prefer

> Teams can now require approval before a generated response is published.

---

## SL-020 Add-on analysis

### Detect

Flag participial tails that append vague interpretation after a concrete statement.

Common forms:

- highlighting...
- underscoring...
- demonstrating...
- reflecting...
- reinforcing...
- signaling...
- showcasing...

### Decision test

Ask whether the appended clause adds a specific inference supported by evidence.

If it simply tells the reader how to interpret the sentence, remove it.

### Do not flag

Keep participial clauses when they describe a real simultaneous action or consequence.

### Avoid

> The company added an approval log, underscoring its commitment to transparency.

### Prefer

> The company added an approval log that records who approved each change.

---

## SL-021 Reader-value instruction

### Detect

Flag phrases that tell the reader what to regard as meaningful.

Examples:

- importantly
- notably
- critically
- what matters most
- the key point is
- the real takeaway
- it is worth noting

Also flag empty importance markers such as:

- "This matters."
- "This matters because..."
- "Why this matters:"
- "What matters here is..."
- "The important thing is..."

These constructions often tell the reader that something is important instead of stating the concrete consequence that makes it important.

### Decision test

Present the relevant fact first.

If its importance is not evident, explain the consequence.

If "this matters" can be replaced by the actual consequence without losing meaning, prefer the consequence.

### Do not flag

Explicit prioritization can be useful in instructions, warnings, executive summaries, or user-requested analysis.

Do not ban every use of matters. A concrete use is fine:

> Timing matters because the token expires after 60 seconds.

### Avoid

> Importantly, administrators can revoke access.

### Prefer

> Administrators can revoke access immediately.

### Avoid

> This matters because the agent may continue after a failed action.

### Prefer

> A failed action may be returned to the model as another problem to solve, allowing the run to continue past the intended stopping point.

---

## SL-022 Totalizing statement

### Detect

Flag claims that compress a nuanced issue into a sweeping declaration.

Examples:

- everything changes when...
- this changes the way we think about...
- the entire model depends on...
- this is what it all comes down to...

### Decision test

Check whether the source supports the stated scope.

Narrow the claim to the actual consequence.

### Do not flag

Keep broad statements when the underlying evidence genuinely supports broad scope.

### Avoid

> This changes everything about how companies use AI.

### Prefer

> The feature changes how teams review generated responses before publication.

---

## SL-023 Pseudo-profound compression

### Detect

Flag short abstract statements whose primary function is to sound insightful.

Signals:

- abstract nouns
- omitted mechanism
- universal tone
- memorable rhythm
- little new information

### Decision test

Ask what observable claim the sentence makes.

If it cannot be translated into something concrete, remove or expand it.

### Do not flag

Concise principles are appropriate when the user explicitly asks for slogans, aphorisms, speeches, or brand lines.

### Avoid

> Trust is the architecture of scale.

### Prefer

> Larger teams need permissions and audit logs because more people can change the system.

---

## SL-024 Micro-manifesto language

### Detect

Flag strings of declarative statements written like a manifesto.

Examples:

> Less noise. More signal. Better decisions.

> No friction. No compromise. Just results.

### Decision test

Ask whether the fragments communicate facts or mainly create attitude.

### Do not flag

Keep this style when the user explicitly requests campaign copy, slogans, manifesto writing, or similar advertising language.

### Avoid

> Less friction. More focus. Better work.

### Prefer

> The integration removes the manual export step from the review workflow.

---

## SL-025 Inflated stakes

### Detect

Flag escalation from a narrow topic to broad consequences without evidence.

Examples:

- the future of work
- the future of AI
- existential
- era-defining
- reshaping the industry
- determining who succeeds
- changing how society...

### Decision test

Trace the claimed consequence.

If intermediate causal steps are missing, narrow the statement.

### Do not flag

Broad stakes are appropriate when the source directly supports them.

### Avoid

> Getting this right will determine which companies survive the AI transition.

### Prefer

> Poor review controls can expose incorrect generated content to customers.

---

## SL-026 Abstract noun stack

### Detect

Flag sentences where several nominalizations carry the meaning while actors and actions disappear.

Common nouns:

- alignment
- enablement
- optimization
- orchestration
- transformation
- implementation
- prioritization
- operationalization
- acceleration
- facilitation

### Decision test

Ask:

- who acts?
- what do they do?
- what changes?

Rewrite around those answers when available.

### Do not flag

Abstract nouns are legitimate in technical, legal, academic, or organizational contexts when they name established concepts precisely.

### Avoid

> The implementation enables optimization of cross-functional alignment.

### Prefer

> The workflow lets product and support teams review the same request before approval.

---

## SL-027 Concept labeling

### Detect

Flag a sentence that explains something and then invents an abstract label for the explanation.

Common forms:

- this is operational trust
- this is adaptive governance
- call this...
- this creates what we call...
- that is the real meaning of...

### Decision test

Ask whether the label will be reused as a necessary concept.

If not, end after the explanation.

### Do not flag

Keep defined terms when the document genuinely needs terminology for later reasoning.

### Avoid

> Reviewers can inspect every approval and reversal. This is operational trust.

### Prefer

> Reviewers can inspect every approval and reversal.

---

# Evidence, attribution, and scope

## SL-028 Unnamed authority

### Detect

Flag claims attributed to vague groups.

Examples:

- experts say
- researchers believe
- critics argue
- observers note
- industry leaders agree
- many professionals say

### Decision test

Identify the source.

If no identifiable source exists, either remove the attribution or make a narrower unsupported claim only when appropriate.

### Do not flag

Broad attribution can be acceptable when summarizing genuinely established consensus and the context does not require citations.

### Avoid

> Experts agree that human review is essential.

### Prefer

> The policy requires human review before publication.

---

## SL-029 Vague evidentiary coverage

### Detect

Flag language that implies evidence without identifying what evidence exists.

Examples:

- research shows
- studies indicate
- data suggests
- reports have found
- evidence demonstrates

### Decision test

Ask:

- which research?
- which data?
- what population?
- what period?
- what result?

If none is available, do not imply evidence.

### Do not flag

Keep the construction when the source is cited or clearly established in context.

### Avoid

> Research shows that these workflows dramatically improve trust.

### Prefer

> In the supplied survey, 61% of respondents said the approval log made review easier.

---

## SL-030 Invented first-person experience

### Detect

Flag first-person claims that imply lived, observed, tested, or witnessed experience the model does not possess.

Examples:

- I've seen...
- in my experience...
- when I tested this...
- we found...
- I noticed...

This includes invented reactions such as "this stayed with me" or "I kept coming back to this" when the source does not establish that the writer actually had that reaction.

### Decision test

Identify whose experience is being described.

Do not fabricate a speaker.

### Do not flag

Preserve first-person statements supplied by the user or explicitly written on behalf of a known speaker when supported by their material.

### Avoid

> I've seen teams cut review time in half with this approach.

### Prefer

> The supplied case study reports a 48% reduction in review time.

---

## SL-031 Unsupported absolute

### Detect

Flag universal or categorical claims that exceed the evidence.

Common terms:

- always
- never
- every
- none
- everyone
- completely
- entirely
- impossible
- guaranteed
- universally

### Decision test

Look for counterexamples or unexamined conditions.

Choose the narrowest accurate scope.

### Do not flag

Keep absolutes in definitions, mathematical statements, hard system constraints, or well-supported factual claims.

### Avoid

> Generated text always contains these patterns.

### Prefer

> Generated text often contains several of these patterns.

---

## SL-032 Fake precision

### Detect

Flag exact numbers, percentages, time estimates, rankings, counts, thresholds, or measurements that were not provided or derived.

### Decision test

Find the source of the number.

If it has none, remove it.

### Do not flag

Keep numbers supplied by the user, calculated from available data, or retrieved from a verified source.

### Avoid

> This approach can improve clarity by 40%.

### Prefer

> This approach removes repeated claims and unnecessary rhetorical structure.

---

# Openings, transitions, and endings

## SL-033 Generic opener

### Detect

Flag openings that provide broad atmosphere without useful task-specific information.

Common forms:

- In today's rapidly evolving world...
- In an increasingly complex landscape...
- As technology continues to advance...
- When it comes to...
- In a world where...
- X has never been more important.

### Decision test

Ask whether the first sentence contains information specific to this subject.

If not, begin closer to the actual point.

### Do not flag

Broad framing can be appropriate in speeches, essays, or pieces where historical context is substantively relevant.

### Avoid

> In today's rapidly evolving AI landscape, businesses face unprecedented challenges.

### Prefer

> Teams using generated content need a review process for factual errors and unsupported claims.

---

## SL-034 Mechanical signposting

### Detect

Flag transitions that announce the structure instead of advancing it.

Examples:

- first, let's explore
- now let's turn to
- moving on to
- another important consideration
- with that in mind
- having established that
- it is worth considering

### Decision test

Start directly with the next idea.

Keep the signpost only if readers genuinely need orientation.

### Do not flag

Signposting is useful in long technical documents, lectures, tutorials, and complex arguments.

### Avoid

> Now that we've covered the benefits, let's look at implementation.

### Prefer

> Implementation starts with the approval rules.

---

## SL-035 Rhetorical question with immediate answer

### Detect

Flag questions used only as setup for the next sentence.

Example:

> Why does this matter? Because...

### Decision test

If the writer already intends to answer immediately, convert the pair into a direct statement.

### Do not flag

Keep real questions in FAQs, interviews, teaching material, dialogue, or when the reader is genuinely invited to consider the answer.

### Avoid

> Why does this matter? Because reviewers need context.

### Prefer

> Reviewers need context to evaluate the request.

---

## SL-036 Reflective framing

### Detect

Flag phrases that introduce commentary about thinking rather than the subject itself.

Examples:

- it is useful to think of...
- one way to view this...
- it helps to remember...
- consider what happens when...
- think about it this way...

Watch for manufactured personal-reflection framing such as:

- "This stayed with me."
- "That line stayed with me."
- "I kept coming back to..."
- "I found myself thinking about..."
- "What struck me was..."
- "I couldn't stop thinking about..."

These phrases can manufacture a personal reaction instead of explaining what is notable about the material.

### Decision test

State the model, comparison, or fact directly.

Ask whether the personal reaction is genuine source material or whether it was introduced by the model to create intimacy or significance.

If the reaction was not supplied by the writer, state the observation directly.

### Do not flag

Reflective framing is useful in teaching when it genuinely helps introduce a difficult mental model.

Do not flag genuine first-person reflection when the user is writing from personal experience and that reaction is part of the intended voice.

### Avoid

> It helps to think of the queue as a living system.

### Prefer

> The queue changes whenever requests are added, approved, rejected, or reassigned.

---

## SL-037 Generic conclusion

### Detect

Flag endings that recap the obvious or add generic optimism.

Common forms:

- ultimately...
- in conclusion...
- as we move forward...
- the future is bright...
- by embracing...
- X will continue to play an important role

### Decision test

Remove the final paragraph.

If nothing useful disappears, delete it.

### Do not flag

Formal academic, legal, or requested essay formats may require explicit conclusions.

### Avoid

> Ultimately, organizations that embrace these principles will be better positioned for the future.

### Prefer

> Administrators can export the approval log as CSV for external review.

---

## SL-038 Quotable or mic-drop ending

### Detect

Flag short final sentences designed mainly for impact.

Signals:

- compressed abstraction
- parallel syntax
- strong cadence
- slogan-like certainty
- no new information

### Decision test

Ask whether the final sentence would look natural on a quote card.

If yes, verify that it also adds information.

### Do not flag

Keep memorable endings when the user explicitly wants speeches, advertising, manifestos, or persuasive rhetoric.

### Avoid

> The future belongs to those who keep humans in control.

### Prefer

> The policy takes effect on October 1.

---

## SL-039 Chat residue

### Detect

Flag conversational assistant language that remains inside a deliverable.

Examples:

- sure
- absolutely
- here's a polished version
- hope this helps
- let me know if you'd like...
- of course
- happy to help

### Decision test

Ask whether the phrase belongs to the artifact itself.

### Do not flag

Keep conversational language when writing an actual chat message and it suits the speaker.

### Avoid

> Absolutely! Here's a cleaner version of the announcement:

### Prefer

Return the announcement itself.

---

# Vocabulary, formatting, and surface habits

## SL-040 Model-favored vocabulary cluster

### Detect

Flag clusters of words frequently used as generic sophistication markers when simpler wording would be more exact.

Examples include:

- delve
- navigate
- landscape
- realm
- robust
- seamless
- elevate
- unlock
- empower
- leverage
- foster
- underscore
- pivotal
- transformative
- holistic
- nuanced
- dynamic
- multifaceted
- tapestry
- cornerstone
- testament
- paradigm

Do not flag a word solely because it appears on this list.

### Decision test

Ask whether the word is the most precise and ordinary choice for the sentence.

The stronger signal is repeated use across a passage.

### Do not flag

Keep a listed word when it is normal terminology in the domain or clearly the best word.

### Avoid

> The robust platform empowers teams to seamlessly navigate a dynamic compliance landscape.

### Prefer

> The platform lets teams review compliance requests and record approvals.

---

## SL-041 Inflated substitute for a simple verb

### Detect

Flag phrases that avoid ordinary verbs such as `is`, `has`, `uses`, `shows`, or `does`.

Examples:

- serves as
- stands as
- represents
- functions as
- boasts
- offers up
- provides users with the ability to

### Decision test

Replace the phrase with a simple verb.

If the meaning stays the same, prefer the simpler construction.

### Do not flag

Keep the longer form when it adds a real semantic distinction.

### Avoid

> The dashboard serves as a centralized hub for review activity.

### Prefer

> The dashboard shows review activity in one place.

---

## SL-042 Em-dash dependence

### Detect

Flag repeated em dashes used to manufacture emphasis, interruption, or afterthought rhythm.

### Decision test

Try a period, comma, colon, parentheses, or sentence rewrite.

Choose punctuation based on syntax.

### Do not flag

An occasional em dash is legitimate when it naturally marks an interruption or strong break and the requested house style allows it.

### Avoid

> The problem is familiar—teams have the data—but they cannot act on it.

### Prefer

> Teams have the data but cannot act on it.

Do not "fix" the sentence by replacing every dash with a semicolon.

---

## SL-043 Unnecessary formatting

### Detect

Flag formatting used to manufacture importance or structure.

Examples:

- bolding ordinary nouns
- a heading for every short paragraph
- label-colon bullets where prose would read better
- bullet lists containing connected reasoning
- excessive italics
- decorative emoji

### Decision test

Remove the formatting.

If comprehension does not decline, keep the simpler form.

### Do not flag

Use formatting when it improves scanning, navigation, comparison, or procedural clarity.

### Avoid

> **Visibility:** See every request.  
> **Control:** Approve every change.  
> **Confidence:** Know what happened.

### Prefer

> The dashboard shows every request and records who approved each change.

---

## SL-044 Fake casualness

### Detect

Flag deliberate attempts to appear human through forced informality.

Examples:

- random fragments
- unnecessary slang
- "kinda," "honestly," "pretty much"
- fake self-corrections
- staged hesitation
- excessive contractions
- conversational filler inserted into formal prose

### Decision test

Ask whether the speaker would naturally use the expression in this context.

Natural writing does not require deliberate imperfection.

### Do not flag

Keep casual language when it matches the user, genre, audience, or supplied reference samples.

### Avoid

> So yeah, the whole thing is kinda messy, honestly.

### Prefer

> The current workflow has several overlapping approval steps.

---

## SL-045 Pattern substitution

### Detect

Flag revisions that remove the visible form of a pattern while preserving its rhetorical function.

Common substitutions:

- `not X but Y` → `rather than X, Y`
- em dash → semicolon
- triad → group of four
- `delve` → `unpack`
- generic conclusion → synonymous recap
- slogan → different slogan
- repeated keyword → mechanical synonym rotation

### Decision test

Compare the original and revised sentence structurally.

Ask whether the rhetorical device disappeared or merely changed costume.

### Do not flag

A surface substitution is fine when it genuinely improves syntax and the underlying structure is legitimate.

### Avoid

Original:

> This isn't about speed. It's about control.

Weak revision:

> Rather than focusing on speed, the focus should be control.

### Prefer

> The approval setting lets administrators decide who can publish a response.

---

# Cross-pattern decision rules

## Prefer functional diagnosis

Do not identify a pattern from vocabulary alone.

Diagnose what the sentence is doing.

For example:

> The system is not available while maintenance is running.

contains negation but is not manufactured contrast.

> The product isn't about automation. It's about trust.

uses negation to manufacture rhetorical opposition and should normally be revised.

## Prefer density over isolated occurrence

One rhetorical construction may be natural.

Repeated constructions are stronger evidence of formulaic writing.

Inspect:

- nearby sentences
- paragraph endings
- section endings
- headings
- the entire document

## Preserve legitimate domain language

Do not rewrite established terminology merely because it sounds formal.

Examples:

- legal terms
- medical terms
- engineering terms
- academic concepts
- product names
- standardized process names
- regulatory language

Precision outranks stylistic variety.

## Preserve legitimate repetition

Do not remove repetition that exists for:

- safety
- legal clarity
- procedural consistency
- specification
- teaching
- deliberate emphasis requested by the user
- stable terminology

Remove repetition whose only function is rhetorical reinforcement.

## Do not flatten voice

The goal is not minimal prose at all costs.

Natural writing can contain:

- humor
- personality
- unusual syntax
- fragments
- strong opinions
- long sentences
- short sentences
- repetition
- metaphor
- rhetorical devices

Preserve them when they appear intentional, appropriate to the genre, and consistent with the user's voice.

## Do not manufacture human flaws

Never improve "human-ness" by intentionally adding:

- spelling mistakes
- grammar errors
- random lowercase text
- false starts
- fake uncertainty
- fake anecdotes
- fake opinions
- invented memories
- arbitrary slang

Naturalness should come from source fidelity, useful information, appropriate structure, and voice.

## Fix substance before cosmetics

When several patterns occur together, revise in this order:

1. unsupported or invented claims
2. semantic repetition
3. artificial structure
4. abstraction
5. inflated rhetoric
6. cadence
7. vocabulary
8. punctuation and formatting

A cosmetic edit cannot repair a structural problem.

## Escalate ambiguous cases

If a pattern remains uncertain after applying this file, read:

`references/examples.md`

Use the longer examples and false-positive cases there before making the final revision.
```