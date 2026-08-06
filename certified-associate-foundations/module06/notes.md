## Governance, Risk, and Responsible Use
_keeps adoption moving safely, exercised by practitioners, one decision at a time_
- the policy sets the boundary, but you are the one who decides, in the moment
- diligence - ownership and verification
- delegation - supplies the criteria for judging whether a use case is appropriate at all

### Appropriate vs Inappropriate
_structured evaluation, not a gut feeling_
- reversibility
- consequence of error
- need for human creativity or empathy
- accountability
#### Delegation criteria for screening

| Criterion                                | The question to ask                                                                                                                |
| ---------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| **Reversibility**                        | Can a wrong output be caught and undone before it causes harm? Irreversible consequences raise the bar sharply.                    |
| **Consequence of error**                 | What is the cost if the output is wrong? Higher consequence demands more human control or rules the use case out.                  |
| **Need for human creativity or empathy** | Does the task require judgment, relationship, or care that AI cannot supply? Some work should stay human regardless of capability. |
| **Accountability**                       | Who is answerable for the outcome, and can that accountability be exercised over an AI-produced result?                            |
>practical rule is to run all four, then ask which one is **load bearing** for this specific use case. The load-bearing criterion is the one that, if it is changed, would move the use case between classifications

#### Classifications
1. Fully appropriate
	- reversible, low consequence, no special human element
	- delegate with normal review
2. Appropriate with human review
	- stakes or accountability require a human gate
	- define the gate explicitly
3. Inappropriate
	- AI should not perform this
	- articulate why not AI and name the human role that must own it

>A defined gate establishes three things: who reviews (the role with the accountability, not whoever is free), what they verify (the specific risk the review exists to catch, such as factual accuracy, fairness, or policy compliance), and when in the workflow the review happens (before the output is used, not after).

### Skill Trust and Feature Level Risk
_source and permissions check before you enable it_
- source
- reach
	- they do not request permission; inherit whatever access the session already has
- appropriateness
	- is it more capability than the job needs
>internal does not mean vetted; may have broad permission for convenience or built against an outdated policy

enable, escalate, or decline
grant the narrowest access that lets the job get done and revisit it when the job changes

### Data Sensitivity, Privacy, and Feature Controls
_data classification is the habit that prevents leakage_
- feature-specific controls are how you act on data classification when persistence or processing is not appropriate
- classify before you upload

1. Safe to Use
2. Review First
3. Keep Out Unless Approved
when unsure treat the data as the more sensitive until confirmation

- partial redaction
	- strip every field that could lead to identification
- redaction that breaks the task
	- redaction is a tool for the case where sensitivity and necessity do not overlap
	- it is not a way to make any data safe

##### Code Execution Sandbox
##### Memory Persistence
- carries information across sessions
- persistence may be what you do not want
##### Incognito Mode
- keeps the session out of your chat history and memory
- still follow your orgs data-retention policies
- can appear in org data exports
- memory exclusion and data retention are separate controls
##### Org-Level Memory Controls
- team plans do not have org-level controls for memory
- enterprise; owners and primary owners hold org-level memory controls including disabling it

>classify first, the pick the control that matches

#### Incognito controls whether something gets remembered; it does not control whether the data was allowed here in the first place

### Organization Policies and Diligence as a Habit
_a policy followed only when someone is watching is not governance_

Diligence - the habit of applying the governance framework consistently, and of auditing real usage against it to close the gaps

>The standard is to apply the framework on the routine, low-visibility decisions, not only on the obvious high-stakes ones, because the routine decisions are where drift accumulates unnoticed.

audit usage against policy regularly
ensure alignment with evolving policy and capability

### Ethical Implications
_ethical risk does not announce itself; it hides in ordinary outputs_
- recognize bias and fairness risk
	- bias can be carried from the prompt, the framing, or the underlying patterns in how language is generated
	- check the output treats people fairly and if framing has tilted the result
- transparency and disclosure
	- disclose ai assistance; the responsible default, when unsure about policy, is to disclose rather than to conceal
- reasoning through ambiguous cases
	- name who is affected
	- ask what could go wrong
	- what does the fair outcome look like
	- what disclosure is called for

>Structured reasoning handles most ambiguous cases, but some situations require more than individual judgment. If the affected population is large, the potential harm is significant, or the ethical question touches areas your team does not have standing to resolve the right move is to escalate rather than decide alone.

# Key Takeaways

#### Governance is a practitioner skill.

Responsible use is exercised one decision at a time, by you, not by the policy binder.
#### Screen use cases with the Delegation criteria.

Reversibility, consequence, human element, and accountability classify a use case as appropriate, appropriate-with-review, or inappropriate.
#### A Skill is software.

Evaluate source and permissions before enabling, the way you would any installed software.
#### Know data sensitivity before it enters a feature.

Classify first, then use Incognito, Memory controls, and redaction to match the handling to the sensitivity.
#### Ethical risk hides in ordinary outputs.

Evaluate for bias, fairness, and disclosure as part of routine review, and reason ambiguous cases through.