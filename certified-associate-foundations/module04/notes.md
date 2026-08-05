## Workflow Integration and Solution Design
_personal habit to repeatable process, run by a team, performing specific steps every time_

#### Delegation
_deciding, for each step, whether the work is AI-appropriate, human-retained, or collaborative_

### Analyzing Requirements and Use Cases
_before you can build anything, the requirements have to be extracted, structured, and pressure-tested_

- turning raw inputs into testable requirements other can act on
- upload raw inputs and ask for a structured analysis, rather than a narrative summary

#### Pressure-testing Requirements
_extraction is the first pass; pressure-testing is what make the output trustworthy_
- ask claude to challenge its own list
>Review the requirements you extracted. Which are ambiguous as written? Which could be interpreted two ways by our proposal team? Which imply a requirement the RFP states only indirectly?

structured list plus a pressure-test pass is a far stronger foundation than either alone; discernment at the requirements stage

### Research, Planning, and Process Optimization
- claude excels at synthesis, calculation must be verified
- synthesis with code-executed analysis
- plan should rest on numbers that were computed, not generated

#### Synthesis
- can synthesis across sources
- information that post-dates training
	- web search for quick lookups
	- research for deeper up-to-date
- verification discipline is important here

#### Code Execution
- when a plan depends on numbers
- use code execution to run calculations

### Solution Design, Development, and Iteration
_design collaborator, not a vending machine_
- ideate, prototype, gather, feedback, and refine; the value loop
- repeat until a solution holds
- running inside a Project
	- keeps context, constraints, and prior decisions stable
#### Ideation
_produces options_
#### Prototype
_makes one option concrete_
#### Feedback
_exposes what is wrong_
#### Refinement
_fixes what feedback exposes_

>Escalation: the moment people rely on it as infrastructure, the build is no longer a prompt-and-iterate exercise

### Delegation Mapping
_AI, a human, or both together_
- before redesigning a workflow map it step-by-step
- decide for each step who owns it

3 criteria for each step for delegation
- reversibility
	- irreversible ones demand human involvement
- stakes
	- high-cost == human-owned or human-reviewed
- accountability
	- does not delegate (approved/rejected, signed, sent, etc)

after delegation mapping ensure the right feature at each step

AI does real work, human owns the decisions and irreversible steps; the redesign

>It is an incorrect approach to give AI more than the risk profile justifies.
- when AI is given an irreversible or high-accountability step that is over-delegation
##### Common mapping errors
**Halo delegation.** A step gets handed to AI because the previous step went well. Each step is judged on its own.
**Collapsing collaborative into automate.** "AI drafts, human reviews" quietly becomes "AI drafts" when the review gate is never actually staffed. A collaborative step with no real reviewer is an automated step.
**Mapping the tool, as opposed to the work.** Teams sometimes map around the features they like (a Skill they built) rather than the actual workflow steps. Map the work first, then adjust the features.

### Communicating Value and Limitations
_credibility comes from accurate claims; limits as well as the value_
- describe capability accurately without inflation or false modesty
- calibrate to the audience
	- match the message to the audience's AI literacy
- document the human oversight
>Handling overstatement: state what the tool does, then identify the human checkpoint.

# Key Takeaways
#### Delegate deliberately, do not automate indiscriminately.

Workflow value comes from choosing which steps Claude does, not from handing Claude everything.
#### Claude is a requirements-analysis partner.

Feed it messy inputs, get structured, traceable, testable needs others can act on.
#### Build plans on verified numbers.

Pair Claude's synthesis with code execution so the figures under a plan are computed, not generated.
#### Map every step against three criteria.

Reversibility, stakes, and accountability decide whether a step is AI-appropriate, human-retained, or collaborative.
#### Communicate limits as clearly as value.

Accurate capability claims with the human review gates named are what earn and keep stakeholder trust.