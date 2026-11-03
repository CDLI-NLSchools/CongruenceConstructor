# Congruence Constructor

Congruence Constructor is a practice app for congruent triangles: which given parts determine a unique triangle, how congruence statements encode vertex correspondence, and how two-column proofs are assembled and checked. In the Constructor, students choose a part-set (SSS, SAS with the included angle, SSA with the angle not included, ASA, AAS, AAA), record a verdict before the construction is revealed, and watch what the givens actually force, including the SSA swinging side (animated), its two-triangle, right-angle, too-long and too-short regimes, and the AAA family of similar triangles. Only after all six part-sets have first verdicts recorded does the app name the four shortcuts, from the student's own data. Later modes cover correspondence statements read off tick and arc marks, proof assembly from statement and reason pieces, and flawed proofs to locate and correct (indicator 5.4).

Math 2201 Unit 8: Properties of Angles and Triangles (indicators 5.6, 5.4)

## How students use it

- Constructor: verdict first, reveal second, for every case. The summary table collects the student's first verdict for each part-set beside what the construction gave.
- Congruence Statements: two congruent triangles, the second rotated or flipped, with side ticks and angle arcs ranked by size. Students match each vertex of ABC to its image; per-vertex feedback points at the marks. A completed match writes the congruence statement in correct vertex order.
- Proof Builder: statement tiles (including distractors the proof does not need) are clicked into rows, and each row takes a reason. Assemblies are checked for completeness, dependency order (givens flexible, corresponding parts only after the congruence), and exact reasons. Four generated families rotate: two triangles on a shared base (SSS), a parallelogram cut by a diagonal (SAS and ASA versions), and a line to the base of an isosceles triangle (SSS).
- Flawed Proofs: a finished-looking proof with exactly one planted flaw (wrong reason, corresponding parts claimed too early, wrong vertex order, or a false given). The student names the step and chooses the correction.

The Proof Record at the bottom collects verdicts, statements, completed proofs and repairs, and serves as the drafting surface the Section 6 portfolio points to. Deliberate distance from assessed work: the proof generator uses no crossing segments (both designated portfolio proofs live on crossing segments, so vertically opposite angles never appear as a proof step here) and no angle bisectors (the test's constructed-response bisector configuration), and its families, givens and conclusions are generated fresh.

## Technical notes

Single HTML file, no dependencies, works offline. All logic is inline in index.html, generation is seeded and reproducible, and a Node harness (harness.js) verifies everything independently: constructed triangles re-measured from their coordinates, SSA outcomes re-derived from the discriminant with all four regimes exercised, correspondences re-derived from side lengths, proof givens and conclusions verified true in their figures, distractor congruences verified false, the assembly checker exercised with valid and broken assemblies, and the safety rails (no bisectors, no interior segment crossings) asserted on every generated proof. Nothing is recorded and nothing leaves the page.

GitHub topics when published: math-2201, angles-triangles, draft (draft removed after QA).
