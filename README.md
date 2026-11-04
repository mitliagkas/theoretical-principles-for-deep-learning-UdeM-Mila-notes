# Theoretical principles for deep learning: scribed lecture notes

LaTeX sources of the scribed lecture notes for **IFT 6169 (formerly IFT 6085), Theoretical principles for deep learning**, a graduate class at Université de Montréal and Mila taught by [Ioannis Mitliagkas](https://mitliagkas.github.io/).

The compiled PDFs, the syllabus and the readings are on the class page: **https://mitliagkas.github.io/ift6169-2023/**

## About the class

Deep learning works remarkably well, but theory lags behind practice. The class goes over recent work that tries to answer questions such as:

- Why can we reliably optimize non-convex objectives?
- How expressive are our architectures?
- Why do large models generalize from far fewer examples than classical learning theory deems sufficient?

Before each new result, the class introduces the tools it needs from optimization, statistics, information theory and statistical mechanics. The notes were written by students, who scribed the lectures in the 2018 to 2021 editions. Each file credits its scribes by year.

Winter 2023 is the last edition of the original class, and these notes are frozen at that version. The class is offered again, with new material, in Winter 2027.

## What is here

- `Lecture NN - <topic>/`: one folder per lecture, with the `.tex` source and its `images/`.
- `Refs/`: the BibTeX files, one per lecture.
- `utils/macros.tex`: shared macros.

Topics covered: convex analysis and gradient descent, smooth and strongly convex optimization, black-box models and lower bounds, Polyak momentum and Nesterov acceleration, SGD, statistical learning theory, PAC-Bayes bounds, stability and generalization, expressivity and universal approximation, random kitchen sinks, the numerics of GANs, and reinforcement learning.

## Building a lecture

From inside the lecture's folder:

```bash
cd "Lecture 06 - Nesterov's Accelerated Gradient, SGD"
pdflatex main_lec6.tex
bibtex main_lec6
pdflatex main_lec6.tex
pdflatex main_lec6.tex
```

Any recent TeX Live or MacTeX works. Lectures 5 and 7 also need the `doublestroke` and `bbm` packages (`tlmgr install doublestroke bbm bbm-macros`), which a full MacTeX install already includes. Known LaTeX errors that remain in some lectures are tracked in [#8](../../issues/8).

## Acknowledgements

Thanks to [Jose Gallego-Posada](https://jgalle29.github.io/), former TA of the class, who first assembled the existing notes in this repository.

## Contributing

Corrections are welcome through pull requests (typos, errors in derivations, broken references). Please keep each PR to one lecture where possible. If you scribed or corrected a lecture, add your name to its scribe list under the right year.
