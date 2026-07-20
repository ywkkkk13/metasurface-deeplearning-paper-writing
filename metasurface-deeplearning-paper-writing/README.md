# metasurface-deeplearning-paper-writing

A Codex skill for writing, rewriting, reviewing, and polishing journal manuscripts on deep-learning-assisted metasurface and metamaterial absorber design.

The skill is particularly optimized for broadband metasurface absorbers, spectral surrogate modeling, forward prediction, inverse design, neural-adjoint optimization, and CST-based electromagnetic validation.

## Features

This skill helps Codex:

* rewrite and polish manuscript sections in journal-level academic English;
* preserve the original argument order, information density, and claim boundaries;
* organize Abstract, Introduction, Methods, Results, Discussion, and Conclusion sections;
* maintain consistent terminology for metasurface absorber research;
* distinguish forward prediction, surrogate modeling, and inverse design;
* improve figure captions, contribution statements, and paper-level argument flow;
* provide Overleaf- and LaTeX-ready replacement text;
* identify unsupported or overstated scientific claims;
* maintain consistency among target, predicted, optimized, and CST-validated spectra.

## Intended Use

The skill is designed for researchers working on topics including:

* deep-learning-assisted metasurface design;
* metamaterial and metasurface absorbers;
* broadband microwave absorption;
* spectral surrogate models;
* attention-, convolution-, or transformer-based spectral prediction;
* neural-adjoint and forward-guided inverse design;
* CST, FDTD, or FEM validation;
* experimental validation and RCS analysis.

The current version contains additional conventions for multilayer ITO/PET/PMI metasurface absorbers.

## Repository Structure

```text
metasurface-deep learning-writing/
├── SKILL.md
├── README.md
├── LICENSE
└── .gitignore
```

`SKILL.md` contains the complete instructions used by Codex.

## Installation

### Option 1: Clone the repository

```bash
git clone https://github.com/ywkkkk13/metasurface-deep learning-writing.git
```

Copy the repository or its `SKILL.md` file into the skills directory used by your Codex environment.

For example:

```text
~/.codex/skills/metasurface-deep learning-writing/
```

The resulting structure should be:

```text
~/.codex/skills/
└── metasurface-deep learning-writing/
    ├── SKILL.md
    ├── README.md
    └── LICENSE
```

Restart or reload Codex after installation when required by your environment.

### Option 2: Download manually

1. Open this GitHub repository.
2. Select **Code → Download ZIP**.
3. Extract the downloaded archive.
4. Copy the extracted folder into your Codex skills directory.
5. Ensure that the main instruction file is named `SKILL.md`.

## Example Requests

After installing the skill, users can give Codex requests such as:

```text
Use the metasurface-deep learning-writing skill to polish this Introduction.
Preserve the original argument order and do not add unsupported claims.
```

```text
Review this manuscript section for terminology consistency.
Use “absorption spectrum” rather than “S11 spectrum” unless the plotted
quantity is actually S11.
```

```text
Rewrite this Results section in journal-level English and preserve all
reported numerical results.
```

```text
Check whether the claims about full-wave accuracy, inverse design, and
experimental validation are supported by the manuscript.
```

```text
Provide the exact replacement LaTeX code and clearly identify the
modification location.
```

## Design Principles

The skill follows several principles:

1. Scientific claims must be supported by the manuscript.
2. Deep learning should be presented as a method for addressing a clearly defined design bottleneck.
3. Forward prediction and inverse design must be described as distinct tasks.
4. Broadband spectra should be treated as frequency-correlated responses rather than independent frequency points.
5. CST or other full-wave validation should not be replaced by unsupported model claims.
6. Rewriting should preserve the author’s original reasoning, information density, and claim boundaries.

## Limitations

* The skill does not verify numerical results unless the relevant data are provided.
* It does not replace electromagnetic simulation or experimental validation.
* Journal-specific formatting requirements should be checked against the latest official author guidelines.
* Some project-specific conventions may need to be modified for material systems other than ITO/PET/PMI absorbers.

## Contributing

Issues and pull requests are welcome.

When proposing changes, please explain:

* the manuscript-writing problem being addressed;
* the proposed instruction change;
* an example showing the expected improvement;
* whether the change is general or project-specific.

## License

This project is released under the MIT License. See `LICENSE` for details.

## Disclaimer

This skill assists with scientific writing and manuscript organization. Authors remain responsible for the correctness of scientific claims, numerical results, citations, simulations, experiments, and compliance with journal policies.
