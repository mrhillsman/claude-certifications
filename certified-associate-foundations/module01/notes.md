>the feature decisions made within Claude _before_ writing a single prompt determine the **quality ceiling** for session outputs

  
1. which entry point to use
2. which capability features to activate
3. which model to select
4. how to manage context across a session

5 Claude behavioral properties regardless of features used
1. responses vary
	- no "one correct response"
	- plan for variation when consistent output is a dependency
	- build review into the process
2. confident tone is not a signal of accuracy
	- a fabricated stat reads the same as a verified one
	- without verification fluency does not signal accuracy
3. context is a budget
	- auto summarization on paid plans with Code Execution enabled
4. knowledge has a training boundary
	- training data has a cutoff date
	- when relevance matters, verify or connect a source
5. configured procedures still produce varied outputs
	- configuration reduces variation but does not remove the need to check the output
	- regardless of how well a skill is built output variance is not eliminated

## Entry Point
_determine where you work_
#### Selection logic

| Task type                                                                                                     | Entry point |
| ------------------------------------------------------------------------------------------------------------- | ----------- |
| One-off question or quick task, no plan to reuse                                                              | Chat        |
| Recurring work with stable context requirements                                                               | Project     |
| Output is a deliverable the recipient will open and read                                                      | Artifact    |
| Requires deep multi-source investigation or synthesis (quick current-information lookups: web search in Chat) | Research    |
### Chat
- default entry point
- unstructured conversation (i question the use of unstructured here)
- works when the work starts and ends in the session
### Projects
- persistent workspaces
- hold three things
	- standing instructions
	- knowledge base
	- conversation history
- solve the most common ai-assisted productivity drain; re-explaining
### Artifacts
- when the desired output is a deliverable
	- draft document(s)
	- data table(s)
	- formatted report(s)
	- code
	- etc
### Research
- goes further than basic web search
- use when deep investigation across a range of sources is needed
- use when synthesis of current information beyond quick lookup is needed

#### Is a project right?
_yes to two or more, build a project_
1. Does this task recur
2. Is the background context the same across sessions
3. Is the output format consistent

## Capability
_what Claude can do within the entry point_
### Skills
_consistent procedures_
- live at the account level
- invoked automatically when relevant in any conversation
- tells Claude to follow a defined procedure consistently wherever it applies

reduce variance but do not eliminate it
require a trust evaluation
	- review its source
	- review permissions
### Code Execution
_verified computation_
- sandboxed computation environment
- produces a verified result by running a calculation
use when
- any numeric output will be used or reported
- data needs to be transformed or cleaned
- output needs to be a chart or a visualization
- output needs to be a real downloadable file
>you want to get away from next token prediction and instead utilize output from legitimate calculation in a sandboxed environment
### Memory
_continuity across sessions_
- retains work-relevant facts across sessions
	- recurring role context
	- preferences for output format
	- names of frequent collaborators
	- standing constraints that apply across projects
most useful when actively curated
- review periodically
- delete or update entries that no longer hold
- keep memory focused on information that genuinely recurs across sessions
>incognito mode
- keeps a session out of memory and chat history
- applies to standalone chats outside projects
- **does not override org's underlying data retention**

## Model Selection
_determines how well Claude does and at what cost in speed_
#### Decision logic

| Task profile                                                            | Model  |
| ----------------------------------------------------------------------- | ------ |
| Routine, structured extraction or classification at volume              | Haiku  |
| Most professional drafting, synthesis, and analysis                     | Sonnet |
| Complex judgment, high-stakes output, ambiguous or multi-layered inputs | Opus   |
### Haiku
_fastest and most efficient_
- handles structured tasks well
- high-volume routine work
	- speed matters
	- cost of imperfect output is low
### Sonnet
_balanced tier_
- right starting point for most knowledge-worker work
- quality falling short - upgrade to Opus
- task is structured, need more speed and volume - downgrade to Haiku
### Opus
_higher-capability tier_
- nuanced judgment
- complex multi-step reasoning
- input interpretation
- work where quality outranks speed
	- client-facing deliverables
	- complex document analysis
	- strategic planning
	- high-stakes synthesis across multiple sources

### Fable
>as of June 2026 the shipped model family includes a fourth tier above Opus (Claude Fable 5, GA 2026-06-09), and Opus-tier latency is currently characterized as moderate rather than slow. The certification pins the three-tier Haiku/Sonnet/Opus frame, so this lesson teaches that frame; treat tier names and characteristics as a verify-at-delivery item. Not exam-relevant.

## Context Strategy
_once what needs to be done is decided, this determines how long it can be done well_

- every conversation has a finite working-memory budget
- budget runs down as conversation grows
- deliberate context management keeps sessions coherent

signs a conversation needs intervention
- Claude stops following instructions as well as it did earlier
- responses lack reference to earlier decisions or context
- accuracy drops in ways consistent with missing context

3 responses to degraded context
1. restart - session has drifted beyond recovery or beginning a new task within the same workstream
2. summarize - ask Claude to produce a summary before staring a new conversation; include things like decisions made, work in progress, open questions, etc.
3. persist - determine if memory or project knowledge base should be updated because saving the right information at the right moment reduces context limit impact

>For intensive tasks, planning ahead is more efficient than working around an interrupted session: break large tasks into segments, save interim progress to the knowledge base, and restart from a summary rather than extending a single session indefinitely.

# Recap

#### Select the entry point before writing the prompt.

Chat handles one-off work. Projects handle recurring work with stable context. Artifacts handle deliverable outputs. Research handles tasks requiring current multi-source information. The entry-point decision shapes every subsequent choice in the session.

#### Four capability layers, four distinct problems.

Projects carry context. Skills define repeatable procedures. Code Execution verifies computations. Memory persists continuity. Use them independently or in combination based on what the task requires.

#### Model tiers reflect a speed-capability trade-off.

Haiku handles structured, high-volume tasks efficiently. Sonnet covers most professional work. Opus handles complex, high-stakes tasks where quality outranks speed. Match the tier to what the task demands.

#### Context is a budget.

Long conversations degrade as context fills. Restart, summarize, or persist. Managing context deliberately is more efficient than working around drift after it has accumulated.

#### Variation is inherent; review is structural.

Every Claude feature, including configured Skills, produces different outputs run to run. Module 3 builds the discipline to evaluate those outputs before they leave your hands. The framework from this module determines the right entry point and capability layer. The framework from Module 3 determines what to do with the output.