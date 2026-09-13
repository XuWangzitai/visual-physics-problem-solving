# Visual routing and simulation design

Read when a representation could materially improve physical reasoning, or before constructing one. Choose the least complex representation that exposes the relevant relationship.

| Reasoning need | Useful representation |
| --- | --- |
| Free-body forces, geometry, rays, coordinates, system boundaries, circuit structure | Labeled static diagram with physically meaningful positions and directions |
| Proportionality, energy landscapes, resonance, functions, scaling, competing models | Graph or a small set of linked plots |
| Forces, velocity, acceleration, electric or magnetic fields, flux, gradients | Vector or field representation; distinguish vector magnitude from display scaling |
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

For prediction-first learning, initialize paused, at baseline, or with outputs hidden. Hide information that would settle the question until a meaningful prediction exists. Use only essential plots and readouts; do not add decorative controls, mandatory worksheets, export panels, or a general application shell.

## Compute dynamics independently of rendering

Use an analytic solution when it accurately represents the model; a sinusoid is appropriate for ideal simple harmonic motion, not a substitute for arbitrary dynamics. For numerical dynamics, choose a solver suited to the equations and timescale. Decouple integration from display refresh: use a fixed simulation timestep with an accumulator, or a controlled solver independent of frames. Bound catch-up work after a pause and keep displayed simulation time honest.

Select timestep and, where applicable, spatial resolution from accuracy and stability needs. Do not prescribe one timestep or integrator for all systems. Stop and explain nonfinite or invalid states instead of silently clipping them into plausible motion. Handle events such as ground impact explicitly. Validate using [physics-validation.md](physics-validation.md) before revealing computed behavior.

Follow the installed `visualize` contract for inline interaction. A standalone offline model is useful when explicitly requested as an export; it is not the default output of this skill. Keep equations and model limitations in the conversation as required by the rendering capability.

For every visual, state what it **preserves**, **simplifies**, and **cannot establish**. For example, a drag trajectory preserves the chosen force law and initial conditions, simplifies the body to a point mass in still air, and cannot establish a real object's drag coefficient. Use equal spatial scales when angles or shapes carry physical meaning, or visibly disclose distortion. Label normalized, clipped, or rescaled vectors and plots.

## Design provenance

General design ideas were inspected in [moving-parts by Changyong Mun](https://github.com/cmun2/moving-parts/tree/e13171e220c0e032712aeac0a7613247ebe00e93) (MIT) and [science-sim-author by dimgouso](https://github.com/dimgouso/science-sim-author/tree/6a32d675acb21c1008a1def87e1eba091dda527c) (MIT): independent simulation time, theoretical comparisons, diagnostic quantities, compact model specifications, and meaningful parameter experiments. This skill contains original instructions; no source code, template, schema, or copied prose from those projects is included. Their standalone file requirements and runtime conventions are not adopted. If future changes incorporate substantial source material, preserve its applicable copyright and license notices.
