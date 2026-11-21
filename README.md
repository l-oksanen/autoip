# Autoformalized linear regularization theory

Linear regularization theory, together with the functional analysis it rests
on, formalized in [Lean 4](https://lean-lang.org/). The mathematics is stated
in the LaTeX blueprint [`blueprint/blueprint.tex`](blueprint/blueprint.tex)
and the Lean source directory [`AutoIp/`](AutoIp/) formalizes it. 

The formalization is meant as a
basis for further autoformalization of inverse problems theory, and along the
way it highlights the declarations in
[Mathlib](https://github.com/leanprover-community/mathlib4) that are relevant
for regularization theory.

## Organization of the source code

The Lean code is organized by the labels of the blueprint. Each part and chapter
of the blueprint, and each statement in it (definition, lemma,
theorem, ...), has a directory named by its LaTeX
label with `_` prepended.

For example, the corollary labelled `cor_tikhonov_apriori` in the chapter
`ch_16_tikhonov` of the part `part_2_reg` is formalized in [`AutoIp/_part_2_reg/_ch_16_tikhonov/_cor_tikhonov_apriori/Spec.lean`](AutoIp/_part_2_reg/_ch_16_tikhonov/_cor_tikhonov_apriori/Spec.lean).
The tests in [`AutoIpTests/`](AutoIpTests/) follow the same layout.

## Pointers for Lean resources

* Kevin Buzzard,
  [Formalising Mathematics](https://www.ma.imperial.ac.uk/~buzzard/xena/formalising-mathematics-2024/)
  ([PDF](https://www.ma.imperial.ac.uk/~buzzard/xena/formalising-mathematics-2024/formalisingmathematics.pdf),
  [Lean repository](https://github.com/ImperialCollegeLondon/formalising-mathematics-2024))
* Lauri Oksanen and Niklas Halonen,
  [Notes on Lean](https://l-oksanen.github.io/lean-notes/)
  ([Lean repository](https://github.com/l-oksanen/lean-notes))

The two complement each other. Buzzard's course notes teach how to formalize
mathematics in practice: they are written for mathematicians, work through
topics such as logic, sets, analysis and algebra with Mathlib, and are
learned mainly by solving exercise sheets with tactics. 

Notes on Lean instead
explain what lies underneath: Lean's type theory as a language for formal
proofs, its kernel primitives (universes, function types and inductive
types), how equality, the natural numbers, type classes and
coercions are built from them, and the axioms Lean adds. 
