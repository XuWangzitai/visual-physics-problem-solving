# Visual routing and simulation design

Read when a representation could materially improve physical reasoning, or before constructing one. Choose the least complex representation that exposes the relevant relationship.

| Reasoning need | Useful representation |
| --- | --- |
| Free-body forces, geometry, rays, coordinates, system boundaries, circuit structure | Labeled static diagram with physically meaningful positions and directions |
| Proportionality, energy landscapes, resonance, functions, scaling, competing models | Graph or a small set of linked plots |
| Forces, velocity, acceleration, electric or magnetic fields, flux, gradients | Vector or field representation; distinguish vector magnitude from display scaling |
| Thermodynamic paths, AC phase, optics, energy levels, spacetime, standing-wave shape | Prefer a static P-V/T-S, phasor, ray, energy-level, spacetime, or node/envelope diagram; add time evolution only when it answers the question |
| Motion, trajectories, oscillations, waves, orbits, coupling, time evolution, parameter sensitivity | Animation or interactive sandbox when changing or stepping an input improves understanding |
| Direct substitution or a relationship already clear from a short equation | No visual; give a brief reason only if useful |

A static free-body diagram often suffices even when the object moves. Add interaction only if it answers a concrete prediction or comparison. For a spatial scientific diagram, use a proper supported graphic, not a node-link diagram that distorts the geometry.

## Specify the physical experiment before building

Derive a compact internal specification from the learner's model and the problem; do not make Thomas fill in a software schema. Identify:

- The learning question, prediction to test, and observable target.
- State variables and units, governing equations, parameters, assumptions, initial and boundary conditions.
- A baseline case, useful parameter ranges, and how each control affects the model.
- The comparison or diagnostic that will test the calculation and its acceptable accuracy.
- What is physically computed, schematically drawn, or deliberately omitted.

Expose one to three meaningful parameter controls when possible. Include units and current values, relevant live readouts, a baseline and reset, and play/pause for time evolution. Reset must restore a reproducible baseline. When parameters change, either reset the experiment or explicitly represent an intervention and account for any injected energy or changed conditions. Playback speed must not change the physical result.

In Learning Mode, obtain and acknowledge a meaningful prediction, direction, model, or approach in chat before emitting an interactive that would settle the current question. A paused visual with an available play or reveal control does not enforce this gate. Before that prediction, a necessary setup visual must omit or conceal decisive traces, results, readouts, and controls so no available interaction reveals the outcome. After the prediction, a paused baseline is appropriate. Deadline Mode has no prediction gate; Check-my-work starts with diagnosis of the submitted work. Use only essential plots and readouts, without decorative controls, mandatory worksheets, export panels, or an application shell.

## Compute dynamics independently of rendering

Compute every displayed physical state from a valid closed-form solution or an integrator of the stated governing equations with the displayed parameter values. Do not substitute keyframes, easing, hand-tuned trajectories, or decorative motion for those equations. A sinusoid is valid for ideal simple harmonic motion, not arbitrary dynamics.

For numerical oscillatory or orbital motion, do not use explicit Euler. Choose a method and timestep that resolve the fastest relevant timescale, including fast transients as well as periods; account for stiffness and spatial stability restrictions where applicable. Refuse or constrain parameters that violate stability instead of clipping results. No single integrator or timestep fits every system.

Decouple integration from display refresh with fixed simulation steps or a controlled solver independent of frames. Bound catch-up work after pauses and keep displayed time honest. Stop and explain nonfinite states, handle impact events explicitly, and disclose numerical limitations. Include a useful benchmark, residual, invariant drift, or error readout when practical; its presence alone is not evidence that a test ran.

A standalone offline model is useful when explicitly requested as an export; it is not this skill's default output.

For every visual, state what it **preserves**, **simplifies**, and **cannot establish**. For example, a drag trajectory preserves the chosen force law and initial conditions, simplifies the body to a point mass in still air, and cannot establish a real object's drag coefficient. Use equal spatial scales when angles or shapes carry physical meaning, or visibly disclose distortion. Label normalized, clipped, or rescaled vectors and plots.

## Design provenance

General simulation-design ideas were informed by [moving-parts by Changyong Mun](https://github.com/cmun2/moving-parts/tree/e13171e220c0e032712aeac0a7613247ebe00e93) and [science-sim-author by dimgouso](https://github.com/dimgouso/science-sim-author/tree/6a32d675acb21c1008a1def87e1eba091dda527c), both MIT-licensed; no code, templates, schemas, or prose were copied.
