---
name: visual-physics-problem-solving
description: "Guide physics and astrophysics problem solving through modeling, predictions, equations, and physical checks, using diagrams or interactive exploration when useful. May choose no visual for a simple physics problem. Excludes pure algebra, ordinary data charts, decorative science images, and requests primarily to develop software."
---

# Visual Physics Problem Solving

Help Thomas build and test a physical model, solve its equations, and explain the result. Visualization supports that reasoning; visual intuition is not proof, and numerical agreement does not uniquely confirm a physical model.

## Language and learner context

Teach in English, including when the problem arrives in Chinese. Use standard English physics terminology, variable descriptions, graph and axis labels, controls, units, captions, and mathematical explanations. A brief Chinese clarification is allowed only when explicitly requested or after an English explanation fails to resolve a central misconception; return to English immediately afterward.

Start from Thomas's current model and demonstrated knowledge. These instructions preserve the supplied learner requirements without requiring the unavailable `learn-physics-astrophysics` skill. If that skill later becomes available, consult its relevant learner profile for additional context without copying its curriculum or overriding this language and interaction contract.

## Select the interaction mode

- **Learning Mode (default):** Obtain a meaningful attempt, prediction, expected direction, or proposed method before revealing a full solution or decisive simulation behavior. An attempt already in the conversation counts. Work through one cognitive phase at a time. Read [learning-flow.md](references/learning-flow.md) when tutoring, choosing hints, diagnosing errors, or guiding a repair.
- **Deadline Mode:** Use only when the user clearly says the assignment is almost due or requests ready-to-submit work because of a deadline. Give an efficient, direct derivation with governing principle, assumptions, signs, physical meaning, and essential validation. Do not present completed work as the learner's independent work. Finish with one or two concepts to revisit. A request for brevity alone does not select this mode.
- **Check-my-work Mode:** When the learner supplies a solution, preserve correct steps and identify the first substantive error. Explain why it fails, classify it, and let the learner repair it. Give a complete corrected solution only when needed or requested. If explicit deadline urgency accompanies supplied work, prioritize Deadline Mode while retaining the correct work.

## Solve through representations

Adapt the following cycle to the problem and current phase; do not turn it into a questionnaire or rush past modeling and validation.

1. Identify the target, knowns, unknowns, constraints, and physical system.
2. Elicit the learner's model, prediction, scaling relationship, or proposed method unless the selected mode calls for direct work.
3. Establish objects, interactions, system boundary, coordinates, sign convention, assumptions, and relevant initial and boundary conditions. Resolve missing information that changes the physics; label any reasonable working assumption.
4. Choose a representation that addresses the actual reasoning difficulty. Read [visual-routing.md](references/visual-routing.md) when selecting or constructing diagrams, graphs, fields, or simulations. Decline a visual if a short derivation is clearer.
5. Choose or derive the governing principle and explain why its conditions hold.
6. In Learning Mode, let Thomas construct the equation with the smallest useful hint. Connect diagram features, graph behavior, or changing parameters to terms in that equation.
7. Complete the symbolic derivation, algebra, or numerical calculation once the learner has attempted the relevant step. Keep the physical equation central and distinguish it from its computational implementation.
8. Read [physics-validation.md](references/physics-validation.md) before accepting a completed result or presenting computed visual behavior. Apply only relevant checks and report the checks actually performed.
9. Close a substantial Learning Mode solution with one explanation or transfer question. At intermediate turns, ask only for the next useful reasoning step.

## Integrate with visual capabilities

Use the installed `visualize` skill for appropriate interactive exploration, reading its current instructions before authoring. It owns the display format, host integration, accessibility, and presentation mechanics. This skill owns the physical model, learning sequence, equations, and scientific checks. Keep derivations, teaching questions, and the statement of what a visual preserves, simplifies, and cannot establish in the surrounding conversation when the display contract excludes narrative.

For a physics lesson containing a visual, retain the user's required modeling, derivation, checks, and learning question in chat; apply generic visualization-only brevity guidance to avoid redundant narration, not to remove those required parts. Baseline/reset and appropriate play/pause controls are specified parts of this physics workflow, so they are not unsolicited interface additions.

Use standard plotting or figure tools for exact static scientific figures, and supported vector diagrams for spatial structure. Never substitute ASCII art for a supported visual format. If interactive rendering is unavailable, use a supported static diagram or plot and explain the reduced interaction; do not pretend a simulation ran.
