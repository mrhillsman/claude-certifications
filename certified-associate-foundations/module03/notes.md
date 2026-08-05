## Output Eval and Validation
_time saved is small and visible, the cost of an unverified error is large and arrives later_

#### Discernment - critically evaluating output against requirements, sources and standards (how you review)
#### Diligence - deciding when verification is required and taking responsibility for the result (why you must review)

- learn to evaluate output systematically
- recognize failure patterns
- build verification into your prompts
- know the thresholds where human review is mandatory
- choose output format that matches the reliability the task demands

## Discernment

### Evaluation
_not a feeling about if output looks good_

Check against three fixed references
- requirements
- sources
- standards

Requirements - does the output reflect what you asked for
Sources - where output relies on documents does it match them
Standards - would this pass in your field

>how is it that a LLM can be conversational when we know at its heart it is driven by probability and is predicted next token based on various hyperparameters but at the end of the day it is predicted next token?

### Hallucinations, Inconsistencies, Bias
_plausible is not the same as verified_

- Claude writes fluently whether it is right or wrong
- you cannot rely on tone or confidence
- know the specific signatures of failure rather than being suspicious of every line

#### Hallucination
- plausible but unsupported claims
	- sounds reasonable, fits topic, no basis in the source or fact
- fabricated specifics
	- invented stats, dates, names, quotes, or citations
- confident tone masking uncertainty
	- a guess and a well-grounded fact arrive in the same assured voice
#### Inconsistencies and Bias
- internal contradictions
	- the whole is rarely held in view at once
	- a claim early on can conflict with one later
- confirmation bias in framing
	- if prompt implies a preferred answer Claude may lean toward it

##### Field Pattern: Completeness Failure
_compare a batch of documents and identify the differences_
- output reads as thorough
- missed differences in the single most important file in the batch
- long documents need a consistency pass not just paragraph-by-paragraph read
>completeness failures concentrate where attention is lowest, and a confident summary of the easy files can mask silence on the hard one

##### Field Pattern: Capability Hallucination
_claim to have taken an action it cannot actually take_
- "i've emailed that to your team"
- "i've saved the file"
>treat any claimed external action as unverified until you confirm it happened

##### Field Pattern: Fabricated Specific
##### Field Pattern: Confident Tone Masking Uncertainty
##### Field Pattern: Internal Contradiction Across a Long Output


### Fact-Checking and Grounding
_strongest verification is built into the prompt, before the output exists_
- prompt for verifiability
	- permit "I don't know"
	- restrict to provided sources
	- require auditable citations
- grounding
	- quote first, then analyze
		- for long documents, extract supporting quotes before drawing conclusions
	- best-of-N comparison
		- re-run the same request and compare
		- runs agree, confidence rises | runs diverge, soft spots that need a human look
	- validate against authoritative sources
		- when a claim matters, check against trusted external reference
#### The techniques as verbatim prompts
- Permission to not know
	- "If the answer is not supported by the documents I provided, say so explicitly rather than estimating. It is acceptable to answer 'the provided materials do not cover this.'"
- Source restriction
	- "Answer using only the attached contract. Do not use general knowledge. For anything the contract does not address, list it under 'Not covered by this document.'"
- Auditable citation
	- "For every claim, cite the section and clause number it comes from, in parentheses, so I can verify it against the source."
- Quote-grounding
	- "Before you analyze, extract the exact sentences from the document that bear on my question. Then base your analysis only on those quotes."

>Before relying on an output ask: did I allow uncertainty, restrict to sources where appropriate, require citations I can audit, and check the high-stakes claims against something authoritative? Building these into the prompt is cheaper than rebuilding trust in the output afterward.

## Diligence

### Human Review
_some outputs must never go out as is, no matter how good they look_
>knowing the thresholds in advance, so the decision to escalate is made by policy, not in the moment after something has already gone wrong

Four Risk Thresholds (demand human review)
- Stakes
	- what is the cost of this wrong? high stakes
- Reversibility
	- can the action be undone? irreversible step
- Audience
	- who sees it? external, executive, and regulatory
- Regulatory Exposure
	- does a rule, contract, or law govern? AI assistance does not remove obligations

##### DO-NOT-SHIP-WITHOUT-REVIEW
- final client deliverables
- audit-critical or financially material calculations
- regulated, confidential, or highly sensitive data
- public or legal communications where misstatement carries lasting consequence

##### Iteration vs Escalation
_more prompting cannot manufacture judgment the situation requires_
- the fast "yes"
	- low stakes, reversible, internal audience, no regulatory exposure
- the deceptive "looks fine"
	- high stakes, executive audience, partly irreversible once presented
- the slow creep
	- high stakes, external deliverable
	- five iterations, rounds 3-5 diminishing returns
	- stop prompting, maybe escalate to a colleague

### Edit and Adapt Output for Audience
_a draft that is accurate is still not finished_

- Clarity
	- cut hedging, tighten loose sentences
	- ai tends toward thoroughness; editing tends toward precision
- Tone
	- match the relationship and the occasion
	- peer vs client vs regulator
- Formatting
	- shape for how it will be read
		- scannable for an executive
		- detailed for a working team
		- clean for an external recipient

>An executive summary leads with the decision and impact
>A working-team version keeps the detail and the method
>An external communication controls what is disclosed and how it is framed

### Output Formats: Inline, Artifacts, Structure, Code-Executed
_format is a reliability decision, not just a presentation choice_

#### Format by purpose
- Inline - quick contextual, not meant to be a standalone artifact
- Artifacts - a separate, editable block you will refine and reuse
- Structured formats - tables and define schemas that downstream tools or readers can consume directly

#### Code execution as the verified-output path
- code execution runs the calculation and returns a computed, checkable result, along with charts and processed files
- determinism attaches to the executed computation

# Key Takeaways
#### Accountability stays with you.
You own every claim in what you ship, whether you wrote it or Claude did. That is why this is the exam's largest section.
#### Evaluate against three references.
Requirements, source material, and professional standards. Run the same check every time and calibrate depth of review to what is at stake.
#### Plausible is not verified.
Fabricated specifics, confident uncertainty, and completeness gaps all read as competent. Learn the signs so you can spot them fast.
#### Build verification into the prompt.
Permit "I don't know," restrict to sources, and require auditable citations. Prevention is cheaper than reconstruction.
#### Know the thresholds in advance.
Stakes, reversibility, audience, and regulatory exposure decide when human review is mandatory. Set the line before the moment, not after.
#### Pick the format by reliability.
When numbers must be right, compute them with code execution rather than generating them as prose.