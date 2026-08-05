## Prompting
_a communication discipline with learnable structure_

Five components of a professional prompt (not needed for every prompt)
1. Role
	- aka persona
	- sets the vocabulary, depth, and assumptions
2. Context
	- unknowable background unless provided
		- audience
		- scenario
		- prior decisions
		- source material
3. Task
	- unambiguous stated primary specific action
4. Constraints
	- what not to do
	- how you keep the output usable without heavy editing
5. Output Format
	- the "shape" of the result
		- table
		- list
		- draft email
		- memo

>Before sending any prompt that matters, run the five components in your head, ask:
>Have I given Claude the role, the context it cannot infer, an unambiguous task, the constraints, and the format I want back?

mind the gaps, do not assume Claude will infer

the components are a powerful tool for prompt diagnostic checklist
- when output falls short, use the components for signal

>**side note:** if you think about the harness, you can have a great one, but still get unusable output not because the harness falls short but rather because the prompt does

## Task Decomposition
_some requests are too large to be a single instruction_

>splitting a multi-part problem into discrete, ordered steps, then running them in sequence rather than asking for everything at once

#### Complex Requests
Example Prompt: "Evaluate these three vendors and tell me which to pick."

In the example, when you provide a "bad" prompt Claude has to invest in understanding the criteria, apply it, weigh trade-offs, and recommend, all in one pass. Claude will gladly do all four but shallowly.

Decomposed Version
- derive criteria and weigh
- score vendors
- raise trade-offs
- recommend

After decomposition, it becomes easier to build on each in the current conversation or move to a separate conversation. I would say this ties into Context Strategy mentioned in previous module.

#### Parallel Cases
_multiple deliverables from a single or shared foundation_

Example Prompt/Scenario: 20-page policy change -> Internal Announcement + FAQ + Executive Briefing

Extract from the foundational data upon which the deliverables are based ensuring complete, relevant, and accurate context to generate the deliverables.

## Prompt Iteration
_an entirely new prompt is not needed; diagnose the output to create the next prompt_

| Symptom                                    | Likely cause                           | Fix                                                                       |
| ------------------------------------------ | -------------------------------------- | ------------------------------------------------------------------------- |
| Output is generic or off-base              | The context was thin                   | Add the background Claude could not infer                                 |
| Output answered the wrong question         | The task verb was ambiguous            | Sharpen the instruction                                                   |
| Output is the wrong length, tone, or shape | A constraint or the format was missing | Add it                                                                    |
| Output is close but misses on one section  |                                        | Iterate on that section only; do not discard a draft that is mostly right |
>think back on the components of a professional prompt

the goal of prompt iteration is not a perfect prompt but instead usable result. recognizing diminishing returns is woven into the idea.

## Adapting Strategy by Task Type
_component stack applies but emphasis shifts with task_

- analysis
	- low creative latitude; high specification
	- what to measure, against what standard, how to handle ambiguity
- research
	- clear scope and source discipline
	- require citations so claims are checkable
		- note that citations can come from training data; be careful
	- quick web search just won't do
- drafting
	- audience, tone, and format
	- medium latitude; control the shape, let Claude fill it
- brainstorming
	- loose constraints; high latitude
	- give goal and boundaries, ask for volume and range

|Task type|What to tighten|What to loosen|
|---|---|---|
|**Analysis**|Criteria, standards, scope|Phrasing|
|**Research**|Question, sources, citations|Synthesis approach|
|**Drafting**|Audience, tone, format|Word choice|
|**Brainstorming**|Goal and guardrails only|Quantity and direction|
>components (prompt structure) the same but the dial between control and latitude moves with the task; decide where you need control and range then set constraints


# Key Takeaways

Five things that hold across this module:
#### Structure drives quality, not cleverness.

Five components (role, context, task, constraints, format) carry almost every professional prompt. Run them before sending anything that matters.
#### Context is the component you will forget.

Claude cannot see what lives only in your head. The most common cause of generic output is a context gap, not a model limitation.
#### Decompose complex work into ordered steps.

Multi-stage requests succeed when each step produces a checkable result and the high-stakes foundation is built first.
#### Iterate on the component that failed.

Read the output as a diagnostic, change the one thing it points to, and stop when rounds stop improving the result.
#### Match strategy to task type.

Analysis wants constraints; brainstorming wants latitude. Decide where you need control and where you need range, then set constraints to fit.