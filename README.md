# Faux Type Theory

These are the materials for the lecture series [Programming language techniques for proof assistants](https://europroofnet.github.io/LFPSI25-Andrej/), delivered by [Andrej Bauer](https://www.andrej.com/en/) at the
[International School on Logical Frameworks and Proof Systems Interoperability (LFPSI)](https://europroofnet.github.io/LFPSI25/),
a [Final EuroProofNet Symposium](https://europroofnet.github.io/Symposium/) event that took place at [Institut Pascal](https://www.institut-pascal.universite-paris-saclay.fr/) on September 8–12, 2025.

The lectures are going to be recorded. A link to the videos will be provided here.

## Lecture 1: From declarative to algorithmic type theory

We study **Faux type theory**, a small type theory with a universe containing itself, dependent products, and local
definitions. We present the theory in traditional declarative style. We then reformulate it to obtain an algorithmic
presentation suitable for implementation.

Material:

* [Lecture 1 slides](./slides/PL-for-PA-lecture-1-handout.pdf)
* [Lecture 1 video](https://youtu.be/jt-LZ7Nycfk?si=x-mAiwiYd_Wrkzjo)

## Lecture 2: A monadic type checker

We implement Faux type theory in OCaml. We use external libraries for parsing and management of bound variables.
The core type checker uses *monadic-style* implementaion that encapsulates the context in a reader monad.

Material:

* [Lecture 2 slides](./slides/PL-for-PA-lecture-2-handout.pdf)
* [Lecture 2 video](https://youtu.be/34W7KZ6zk4I?si=Pz3QKzz3NXqjklZK)
* Lecture 2 Implementation: [`monadic-fauxtt`](./monadic-fauxtt)


## Lecture 3: Holes and unification

Holes are parts of a term that the user has not provided. They can be filled in by a number of mechanisms: unification,
type class resolution, interaction with the user, automated search, etc. In type theory, they appear as meta-variabales.
We will look at a rudimentary implementation with holes that fills them in using unification.

Material:

* [Lecture 3 slides](slides/PL-for-PA-lecture-3-handout.pdf)
* [Lecture 3 video](https://youtu.be/hS8_RwDvilo?si=ZZIwGTdEgMcc5d94)
* Lecture 3 implementation:** [`holey-fauxtt`](./holey-fauxtt)

## Lecture 4: Variables as computational effects

After a review of algebraic effects and handlers, we implement variables and meta-variables as computational effects.
Doing so allows us to remove the monadic-style code and replace it with direct-style naive code.

Material:

* [Lecture 4 slides](slides/PL-for-PA-lecture-4-handout.pdf)
* [Lecutre 4 video](https://youtu.be/hS8_RwDvilo?si=ZZIwGTdEgMcc5d94)
* Lecture 4 Implementation: [`algebraic-fauxtt`](./algebraic-fauxtt)
