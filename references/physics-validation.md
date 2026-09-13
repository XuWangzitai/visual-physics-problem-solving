# Physical and numerical validation

Read before accepting a completed solution or presenting computed visual behavior. Select checks that could falsify this model or calculation; do not claim every check applies or report an unperformed check as passed.

## Check the model and result

- **Dimensions and units:** Terms in an equation must be compatible. Convert inputs consistently and retain units in the result and display. Distinguish dimensionless ratios from dimensional quantities.
- **Coordinates and signs:** Reconcile directions, vector components, work, potential differences, and flux orientation with the declared convention.
- **Initial and boundary conditions:** Substitute the initial state and test endpoints, interfaces, constraints, and event conditions.
- **Zero input and symmetry:** Check the appropriate equilibrium or unforced behavior and symmetries of the actual system. Zero forcing does not imply zero motion when initial energy is present.
- **Limits and scale:** Examine relevant small and large parameters within the model's domain; compare orders of magnitude. A divergent or impossible limit may expose a failed approximation rather than an algebra mistake.
- **Balance laws:** Choose energy, linear or angular momentum, charge, mass, or another invariant according to the system boundary and interactions. For open, driven, or dissipative systems, check input/output or loss terms rather than incorrectly demanding conservation of the subsystem's mechanical energy.
- **Independent comparison:** Compare with a known analytic case, alternative derivation, or appropriate reference result. Agreement tests consistency; it does not prove that the model is unique or describes every real system.

Distinguish an exact result within an idealized model, an approximation, numerical output, empirical fit, analogy, and schematic. State the restrictions that affect the answer and avoid precision beyond the input or numerical accuracy.

## For numerical models

Compare the target observable at a common physical time or event for timestep h, h/2, and, when needed, h/4. For spatial models refine the grid as well. Report the observed change or error against an analytic solution, not merely "stable." Stability is not accuracy. Select tolerances suited to the requested quantity and duration; extend the test when long-term drift matters.

Check a meaningful baseline and a limiting case independently of the implementation. Measure relevant balance residuals or invariant drift. Near a zero invariant, use an absolute or physically scaled error rather than dividing by zero. Do not renormalize away drift to manufacture a passing check. Separate real dissipation from integration error.

For event outputs, such as range at landing, locate the event rather than accepting the first sample below ground. If validation fails, correct the model, method, or claimed scope before using the animation as evidence. Disclose validation that cannot be executed in the available environment.

## Domain checks when relevant

| Model | Particularly useful checks |
| --- | --- |
| Incline or circular motion | Force projections; normal force is not automatically mg; radial net force supplies centripetal acceleration rather than an extra force. |
| Projectile with drag | Drag opposes velocity relative to the medium; state linear or quadratic law and coefficient units; recover ballistic motion as drag vanishes; mechanical energy loss matches drag work. |
| Simple or driven oscillator | Initial phase, frequency units, unforced and undamped limits; balance input power against dissipation; distinguish transient and steady response. |
| Continuity and Bernoulli flow | Mass flow balance; incompressibility where used; Bernoulli's steady, inviscid streamline assumptions and elevation/pressure terms; account for pumps or losses when present. |
| Standing waves and superposition | Endpoint conditions, phase, node locations, wavelength/frequency relation, linearity assumptions, and energy transport versus motion of the pattern. |
| Electric field or potential | Vector superposition versus scalar potential; symmetry; potential reference; E = -grad V; charge singularities and far-field limits. |
| Orbits | Central-force assumptions, energy and angular momentum where conserved, period scaling, orbital shape, and long-duration numerical drift. |
