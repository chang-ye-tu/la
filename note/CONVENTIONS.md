# LA lecture notes: composition contract

Read this file before editing any `note/*.Rnw`. It is the self-contained,
authoritative contract for this course.

## 1. Scope and dependency order

> **No unproved result.**

The notes may assume only:

- the real field axioms and completeness of `ℝ`;
- the following one-variable calculus facts: algebra of limits and continuity;
  the sum, product, quotient, and chain rules; derivatives of polynomials,
  reciprocals, square roots on `(0,∞)`, exponentials, and logarithms; the mean-
  value theorem; the fundamental theorem of calculus; the one-variable second-
  derivative criterion for convexity; and consequences derived directly from
  these facts at the point of use;
- the fundamental theorem of algebra, used only to ensure that a complex
  polynomial of positive degree has a root;
- where distributions occur, the definitions of expectation and variance.

There is no required preliminary appendix. `prelim.Rnw` is an inactive legacy
scaffold: do not edit, build, cite, or use it. It supplies no prerequisite.
Complex arithmetic is defined where first used. Any other needed fact about
polynomials, multivariable calculus, or probability is stated and proved locally
before use.

A unit may use its own earlier results and results from earlier units. It may not
use a later result. Within a unit, cite the earlier labeled result. Across units,
name the earlier topic and restate both the hypotheses and the exact conclusion
used at the point of use; do not print a unit number or a theorem number from
another document.

Apply this document-order test to every definition, result, proof, remark,
derivation, example, computation, pitfall, exercise, and solution. Except in the
definition that introduces it, every symbol, operation, construction, and named
concept must have been defined earlier. A numbered result may assert a new
consequence of earlier material, but its proof immediately follows and the
result is not used before that proof ends. An exercise may ask for a new
consequence of earlier material, but its solution immediately follows. Only the
asserted proposition may be new: every operation, named concept, and hypothesis
in its statement is earlier material. Within a proof, remark,
derivation, example, computation, pitfall, or solution, each non-assumed fact is
proved earlier or derived before its first use. No object may import theory
scheduled for a later unit.

An exercise may introduce local variables and problem-specific objects by
formulas using earlier operations. Such notation is not a license to define a
new operation, named concept, or body of theory inside the exercise.

## 2. Sources and provenance

A&M (Abadir--Magnus) and H (Harville) are co-primary instructor sources; neither
is the default spine. S (Serre) is used when its formulation, proof, or exercise
is better. A&M offers a broad topic order and a large problem bank; H offers
theorem-led statistical matrix algebra. Select independently from both.

Before drafting a unit:

1. search A&M, H, S, and every specialist source routed for that unit for each
   planned definition, result, proof route, example, and exercise;
2. select by mathematical quality, relevance, and prerequisite fit;
3. record the exact printed coordinate before writing;
4. verify that the proof or solution uses only earlier material.

Where H covers a theory period, a central result or proof route in that period is
H-derived. An isolated definition, co-citation, or exercise does not satisfy this
rule. If H does not cover the topic, do not pad the citations.

Every numbered object has exactly one provenance line immediately before its
closing environment. Choose one form:

```tex
\origin{A\&M Ex.~3.12}
\origin{H Lemma~16.1.2}
\origin{S Prop.~1.3}
\origin{A\&M Ex.~3.12; H Thm.~4.3.8}
\origin{Adapted from A\&M Ex.~3.12}
\origin{Course formulation from H Lemma~16.1.2}
\origin{Course formulation}
```

This applies to every `definition`, `theorem`, `lemma`,
`proposition`, `corollary`, `example`, and `exercise`. List all
sources that materially determine the statement, proof, or solution. The tag on
a result covers its immediately following proof; the tag on an exercise covers
its immediately following solution. Use `Adapted from` when the statement or
argument is materially modified, and `Course formulation from` when the notes
give a new formulation materially determined by a source. Use `Course
formulation` only for genuinely new course material, never for an omitted source
search. A missing or vague tag is a failed audit.

Use a numbered theorem, lemma, proposition, exercise, equation, or section. If
the passage has no numbered locator, give its printed page. A bare chapter is
not an exact coordinate.

Do not quote an imported result only in running prose. State it as a tagged
numbered object, or invoke a result already proved in these notes according to
the within-unit and cross-unit rules above.

An origin tag records provenance; it never licenses an unproved external
result.

The local instructor copies are not distributed.  In the paths below, `${LLM}` denotes the
local research/LLM-project root and `${LEC}` the local lectures root; neither location is a
runtime dependency of the public build.

| Abbrev. | Source | Local path |
|---|---|---|
| A&M | Abadir and Magnus, *Matrix Algebra* | `${LLM}/books/ma/ma_NN.tex` |
| H | Harville, *Matrix Algebra From a Statistician's Perspective* | `${LLM}/books/harville/harville_NN.tex` |
| S | Serre, *Matrices: Theory and Applications*, 2nd ed. | `${LLM}/books/serre/serre_NN.tex` |
| MC | Magnus, *A Gentle Introduction to Matrix Calculus*, expanded | `${LEC}/mva/note/mc.tex` |
| CLM | *Classical Linear Models* | `${LEC}/mva/note/clm.tex` |

Students are not assigned any of these books. Units contain no `reading`
environment, and exercises are rewritten for the notes rather than copied.

## 3. Mathematical writing

Allowed prose and theorem environments:

- `definition`;
- `theorem`, `lemma`, `proposition`, `corollary`;
- `proof`;
- worked `example`;
- `exercise` followed immediately by `solution`;
- a short factual `remark` or mathematics-only `derivation`;
- two commented source markers, `% \periodmark{End of period N of 3.}`, at the
  period boundaries. They are not typeset.

A completed unit contains no `sketch`, `plan`, `reading`,
`motivation`, or `suppremark` environment.

Each theory section begins immediately with its first subsection, and each
theory subsection begins with a numbered mathematical object. A computation or
pitfall subsection begins directly with its formula, code, or diagnostic. The
Exercises section begins with its first exercise. Delete:

- lead-ins announcing a definition, proof, example, calculation, comparison, or
  code chunk;
- summaries, previews, rhetorical framing, and “why this matters” asides;
- meta-commentary about the document;
- prose that merely repeats a displayed formula or printed number;
- hardcoded internal section numbers;
- em-dashes (`---`) in `.Rnw` files.

Necessary notation belongs in the definition or statement that first uses it.
Do not announce a forward debt; defer the material until its prerequisites have
been proved.

### Proof register

Proofs, solutions, and derivations are concise, exact, and algebraic.

- Use equality chains, equivalences, implications, indexed sums, block
  identities, and set inclusions whenever they state the step exactly.
- Prose may introduce variables, split genuine cases, cite the result licensing
  a step, or close the argument. It does not narrate algebra already displayed.
- Prefer
  `x\in\ker T\iff T(x)=0\iff\cdots`
  to a paragraph describing the same implications.
- Delete filler claims such as “clearly”, “obviously”, “easy”, “one can see”,
  bare “standard”, and “the result follows”; write the step.
- Prove both directions of equivalences, equality cases, zero-dimensional cases,
  and conformability conditions when they occur.
- Theory uses exact quantities. Decimal evidence and tolerances belong in
  §Computation.

Worked examples use small exact matrices unless numerical behaviour is the
subject. A course-formulated example must expose a structure used later, not
serve as arithmetic practice.

## 4. Exercises

Exercises form one flat list, each with a complete but compact solution and an
`\origin` tag.

Every exercise has transfer value and belongs to at least one of these types:

- an identity or lemma used in a later unit;
- a proof device worth reusing;
- a counterexample that distinguishes nearby concepts;
- a construction or characterization;
- a structural diagnostic for a matrix or statistical model;
- an application that connects two parts of the unit.

Reject repetitive row reduction, routine multiplication or determinant drills,
parameter substitutions with no new idea, and disguised copies of worked
examples. The set must mix proof, construction, counterexample, and application.
Only the proposition asserted by an exercise may be new. Every operation, named
concept, and hypothesis in its statement must be earlier material. Each
solution step may use earlier course material and facts already
derived in that solution. A later part may use an earlier part only after its
proof. An exercise may use an earlier exercise only after that earlier solution.
Local variable names and formula-defined problem data are permitted; new
mathematical vocabulary and operations are not.

## 5. Computation

Every unit has §N.4 `Computation: Numerical Checks in R`. It verifies selected
theoretical identities and numerical behaviour with several small live chunks.
Use built-in R linear-algebra functions whenever they provide the operation.

- For an identity or decomposition, compute the relevant quantities by two
  mathematically equivalent routes, then print their difference or
  reconstruction residual.
- When algebraically equivalent routes have different numerical behaviour,
  compute both.
- Run every numerical claim before retaining it.
- State the routine, method, and tolerance for numerical rank or definiteness.
- Print residuals or small values, not booleans that rounding can flip.
- Use `symmetric = TRUE` for symmetric eigenproblems.
- Compare eigenvectors through `|q'q_tilde|` or projectors because signs are
  arbitrary.
- Do not oversell timing differences that the printed output does not support.

Recurring comparisons include decomposition reconstruction, normal equations
against QR, Cholesky against a symmetric square root, numerical rank across
tolerances, and predicted digit loss from a condition number.

## 6. Course structure

Fourteen teaching weeks, three 50-minute periods per week; midterm in week 9 and
final in week 16.

| Wk | Unit | Topic |
|---:|---:|---|
| 1 | U01 | Vectors, Matrices, and the Data Matrix |
| 2 | U02 | Vector Spaces, Basis, Dimension |
| 3 | U03 | Rank, Inverse, and Determinant |
| 4 | U04 | Partitioned Matrices and the Schur Complement |
| 5 | U05 | Systems of Equations and Elimination |
| 6 | U06 | Orthogonality and Projection |
| 7 | U07 | Eigenvalues and Eigenvectors |
| 8 | U08 | The Spectral Theorem |
| 9 |  | Midterm, U01--U08 |
| 10 | U09 | Positive (Semi)definite Matrices |
| 11 | U10 | Idempotent Matrices and Quadratic Forms |
| 12 | U11 | The Singular Value Decomposition |
| 13 | U12 | Kronecker Product, vec, and Patterned Matrices |
| 14 | U13 | Matrix Differential Calculus I |
| 15 | U14 | Second Differentials and the Linear Model |
| 16 |  | Final, U09--U14 |

Each unit has three theory sections, one per period, followed by §N.4
Computation, §N.5 Pitfalls, and §N.6 Exercises. Place
`% \periodmark{End of period N of 3.}` between theory sections: retain exactly
two such source comments, but leave both invocations commented out so no
period-end banner appears in the PDF.

Out of scope: Jordan form and A&M ch. 9; Hilbert spaces and A&M §3.3; most of
A&M ch. 12 except inequalities actually used; complex vector spaces beyond the
finite-dimensional facts introduced locally for characteristic polynomials and
Schur triangularization.

## 7. Source routing

This table is instructor-facing. It routes the initial source audit; exact
coordinates belong on the numbered objects.

| U | A&M route | Harville route | Other route |
|---:|---|---|---|
| 1 | chs. 1--2, §5.1 | chs. 1--2, 5--6; §14.6 | S §§1.1, 1.3 |
| 2 | §3.1; §4.1 | ch. 3; §§4.1--4.4, 7.2, 11.1--11.2, 17.1, 17.4, 22.1--22.4 | S §§1.1--1.2, 2.2 |
| 3 | ch. 4 | §§4.4--4.5, 7.4, 17.5; chs. 8, 13 | S §2.2.2.5, Prop. 2.7; §§3.1--3.3 |
| 4 | ch. 5 | §§2.1--2.2, 8.5, 13.3, 18.1--18.2 | S §3.3, Props. 3.9, 3.21 |
| 5 | ch. 6 | §§7.1--7.3, 11.1--11.3, 11.8, 14.5a--b, 14.5e | S §11.1 |
| 6 | §3.2; Exs. 7.34--7.35; §8.3 | chs. 6, 12; §10.2; §§17.6--17.7 | S §§2.3, 11.3; CLM §§2, 8, 11 |
| 7 | §§7.1, 7.3--7.4 | §§21.1--21.7, 21.10 | S §§3.4--3.8, 5.1.1 |
| 8 | §§7.2, 12.4 | §§21.4--21.6, 21.12--21.13 | S §§5.2--5.5, 6.1--6.5 |
| 9 | §§8.1--8.2, 12.1--12.2 | §§14.1--14.5, 14.8--14.9, 18.1, 18.3, 21.9, 21.14 | S ch. 6; §11.2 |
| 10 | §§8.1, 8.3 | ch. 10; §§14.1--14.3, 18.4 | S §5.4; CLM §4 |
| 11 | §8.1, Ex. 8.38; §§10.3--10.5 | §§6.1, 8.4; ch. 20; §21.12 | S §7.1.4, §10.1, §§11.4--11.5; MC §15 |
| 12 | §§10.1--10.4, 11.1--11.3 | §§16.1--16.5 | S §§4.1, 4.3; MC §§2.3--2.6; CLM §2 |
| 13 | §§13.1--13.8, 13.10 | §§15.1--15.8, 15.11, 16.6; §21.15 | MC §§3--8 |
| 14 | §§13.9--13.12 | §§15.9--15.11; ch. 19 | MC §§9--16; CLM §§2--4, 8, 10 |

Use `ISLR2::Boston` for real-data regression demonstrations. Otherwise
simulate from a known truth with `set.seed`.

## 8. Notation and build checks

### Fixed notation

- `\bb` is `\boldsymbol{\beta}`; use `\bbb` for the right-hand side
  of a linear system.
- `\be` is `\boldsymbol{\varepsilon}`; use `\eu_j` for a standard
  coordinate vector.
- Use `\rank`, `\col`, `\row`, `\nul`, and `\spn` for operators. Reserve
  calligraphic letters such as `\calC` for explicitly named sets, spaces, or
  bases.
- Column `j` of `\bA` is `\ba_j`. Row `i`, written as a
  column, is `\tilde\ba_i`; the row is `\tilde\ba_i'`.
- Write all non-strict inequalities with `\leqslant` and `\geqslant`.
  The commands `\le`, `\leq`, `\ge`, and `\geq` are prohibited in unit files.
- Use `\prb`, `\expc`, `\var`, `\cov`, `\cor` or `\corr`, and `\indc` for
  probability, expectation, variance, covariance, correlation, and indicator
  functions, respectively. Do not hand-set these operators with ordinary
  letters, `\mathrm`, or `\mathbb`.
- Check the preamble before adding a notation macro.
- Keep the short `\fancyhead[L]` title under about 36 characters.

### References

- Section references use `§\ref{...}`; named objects use
  `Theorem~\ref{...}`, `Definition~\ref{...}`, and analogous forms. Never type
  a generated number. These forms are within-unit only.
- `\ref` does not cross documents; cross-unit references follow the topic-and-
  hypotheses rule in §1.
- Do not run two builds concurrently; minted temporary files collide.

### Verification

Before building:

- complete the semantic document-order audit required in §1;
- audit the provenance of every numbered object and its proof or solution.

Then, from `note/`:

```sh
python build.py NN
```

A completed unit must have:

- zero build errors and undefined references;
- no unresolved LaTeX warnings, overfull or underfull boxes, `plan`, `sketch`,
  or em-dashes;
- the exact §N.4 heading `Computation: Numerical Checks in R`;
- exactly two commented period-boundary invocations and no active
  `\periodmark` invocation;
- no `\le`, `\leq`, `\ge`, or `\geq`, and no hand-set statistical operator
  superseded by the fixed macros above;
- every R chunk executed successfully during knitting;
- exactly one `\origin` immediately before each numbered object's closing
  environment, with no unmatched `\origin`;
- visual inspection of every page of the generated PDF.

Required R packages are `ISLR2`, `knitr`, `MASS`, `Matrix`, and
`xfun`. `expm` and `pracma` are optional.
