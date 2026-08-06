## Troubleshooting and Optimization
_don't give up, don't make random changes, diagnose_

### Diagnosing Under-performing Prompts and Outputs

##### Common Failure Patterns
- Under-specification
	- leaving out context, constraints, or format
	- fix: add what's missing
- Context overload
	- long session/conversation, context limit approached, earlier content summarized
	- fix: restart or summarize, not a better prompt
- Wrong feature or model
	- prose for calculation instead of code execution
	- deep analysis for haiku rather than haiku for speed
	- fix: use the right tool/model
- Stale configuration
	- fix: maintenance

##### Where do the patterns show up?
- Under-specification
	- from the very first response
- Context overload
	- partway through a good session degradation shows up
- Wrong feature or model
	- specific, repeatable errors; like slightly off numbers or shallow analysis when depth is expected
- Stale configuration
	- "it used to work"

#### Diagnostic Sequence
1. Re-read the prompt
2. Check the conversation length
3. Check the feature and model
4. Check the configuration
5. Question whether the task is a fit

>Run end to end, the sequence usually takes a minute or two and ends in one of two places: a specific, cheap fix (most of the time), or a confident, reasoned "this task needs reshaping" (occasionally).

### Adjusting Approach from Feedback and Results
_every disappointing output is diagnostic data_

##### Build feedback loops into recurring work
A recurring report that needs the same manual correction every week is telling you the prompt, context, or configuration is missing something
##### Translate critique into a specific adjustment
"this isn't quite right" is insufficient. Turn a reaction into an instruction; "too generic", look into the context, "wrong tone", add a tone constraint
- the adjustment should be specific enough to act on and check
- reaction is "how it feels", instruction is "what to change"
##### Capture what worked
When a fix works, do not leave it in a one-off conversation where it will be lost; promote it. Update memory, instructions, configuration, etc.
- configuration is the deliberate, shared, reliable home for a fix
- will this same correction be needed again, by me or someone else?

### Optimizing Workflows for Efficiency and Effectiveness
_optimization is deliberate, not accidental_
- instrument the workflow
- find the friction
- promote the fix into configuration
##### Find redundancy and friction
Signals of removable friction: repetition, correction, and variance
- repetition
	- paste or type the same thing every run?
	- fix: saved context or a standing instruction
- correction
	- fixing the same flaw in every output
	- fix: configuration change so the flaw stops appearing
- variance
	- different people, same task, different results
	- fix: shared skill or knowledge base
##### Consolidate and promote
consolidate steps that can run together and prompt repeated patterns into projects and skills
- promotion requires landing in the right place
- is it a rule, a reference, or a procedure
	- rules go to instructions
	- references go to knowledge
	- procedures go to skills
- promote with caution
##### Measure the improvement
optimization you cannot measure is hard to justify or sustain
- time saved per cycle
- revision cycles reduced
- consistency improved when different people do the same task
- qualitative and quantitative

# Key Takeaways

#### Under-performance has discover-able causes.

Run the diagnostic sequence, specification, context, feature, configuration, before blaming the tool.
#### Isolate before you fix.

Name whether the failure is the prompt, the context, the feature choice, or an expectation mismatch; the cause points to the fix.
#### Every disappointing output is data.

Translate critique into a specific adjustment, then capture the fix as an instruction or Skill so it persists.
#### Optimize deliberately.

Instrument the workflow, find the friction, promote the fix into configuration, and measure the gain.