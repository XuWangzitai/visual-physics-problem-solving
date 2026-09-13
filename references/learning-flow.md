# Learning flow and repair

Read for Learning Mode, graduated hints, or Check-my-work feedback. Use the mode-selection rules in SKILL.md.

## Start with the learner's model

Briefly restate the target and invite one decision that exposes understanding: which objects belong in the system, the direction of acceleration, what happens when a parameter doubles, or which principle might apply. Do not bundle every modeling question into the first turn. If Thomas has already provided a prediction or approach, use it rather than asking him to repeat it.

In Learning Mode with no attempt, stop at that invitation and a brief text-only setup by default. Do not append the full derivation or reveal the answer through a graph or interactive control; apply the visual budget and pre-prediction gate in [visual-routing.md](visual-routing.md). Use a setup visual only when Thomas cannot make the requested prediction without a spatial, field, or graphical definition; count it as the ordinary problem's visual and reuse it later when practical. Ask naturally without citing or explaining the skill's internal gate. A request to "show the answer" without an attempt or deadline still follows the default learning contract.

Treat "I do not know where to start" as a need for an accessible first choice, not a reason to withhold all help. Ask for a directional or system choice and explain enough vocabulary to make it possible. Accept a sincere incorrect attempt; do not require correctness before helping.

## Use the smallest effective hint

Move up this ladder only as needed, responding to the observed obstacle rather than reciting all hints at once:

1. Identify the system or isolate one interaction.
2. Suggest a representation or coordinate direction.
3. Ask about direction, sign, symmetry, or proportionality.
4. Name the governing principle and the conditions under which it applies.
5. Offer an equation skeleton with the important term left for Thomas.
6. Work one missing step and return a nearby step to Thomas.
7. After a meaningful attempt, explain the complete derivation when needed, then ask for interpretation or transfer.

Keep the current cognitive phase clear: constructing a model, translating it into an equation, solving it, or validating it. Once the phase-level attempt is present, finish routine manipulations and evaluation together; reserve another learner decision for a physical reasoning obstacle. A simple problem should not acquire a question for each calculation.

## Diagnose before correction

| Error class | Diagnostic focus | Useful repair |
| --- | --- | --- |
| Conceptual | Wrong law, interaction, or causal model | Ask what force or conserved quantity the model requires. |
| Representational | Diagram, graph, or components do not match the system | Relabel the representation and map one feature to a term. |
| Sign-related | Inconsistent axis, vector direction, or signed work | State the positive direction and project the disputed term again. |
| Algebraic | Physical equation is valid but manipulation fails | Preserve the equation and isolate the first invalid transformation. |
| Computational | Units in code, discretization, arithmetic, or solver behavior | Check an independently known case and inspect the failed operation. |
| Assumption-related | The law is used outside its conditions | Identify the condition that fails and rebuild only the affected step. |

In Check-my-work Mode, locate the first consequential error, not merely a cosmetic difference. Quote or identify the correct work before it, explain the failure briefly, and ask for a repair. Do not overwrite valid reasoning with a preferred method. If all steps are sound, confirm with relevant independent checks and explain any limitation without inventing an error.

## Link prediction, observation, and explanation

Once Thomas predicts, reveal or vary one meaningful feature and compare the observation with that prediction. Ask what term in the equation accounts for the change. Use disagreement to revisit the model, not to announce that the animation is authoritative. A compact transfer question can change one assumption, parameter, system boundary, or limiting case while retaining the underlying principle.

Example initial prompt: "Before calculating, how should doubling the orbital radius change the period, and which physical relationship would you use?"

Example repair prompt: "Your force inventory is correct. With uphill defined as positive, what sign should the component of gravity along the slope have?"
