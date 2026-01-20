# Schemacs
## A clone of Emacs and Emacs Lisp written in Scheme

### See: <https://codeberg.org/ramin_hal9001/schemacs>

The home source code repository for this project is: <https://codeberg.org/ramin_hal9001/schemacs>. This GitHub source repository serves as a redirection pointer to the real home of Schemacs on Codeberg, as well as a place to submit issues for GitHub users.

- Please **do** feel free to submit issues related to Schemacs to this repository.
- Please **do** clone the [code from Codeberg](https://codeberg.org/ramin_hal9001/schemacs) and give it a try!
- Please **do not** clone this GitHub repository or submit PRs.

### Presentations about Schemacs at EmacsConf

- [EmacsConf 2025](https://emacsconf.org/2025/talks/schemacs/)
- [EmacsConf 2024](https://emacsconf.org/2024/talks/gypsum/)

### **NOTE:** This is *not* a fork of [Guenchi's Schemacs](https://github.com/guenchi/Schemacs)

Since [@Guenchi](https://github.com/guenchi) has apparently not had time recently to continue development of her "Schemacs" project, we asked permission of her to name this project "Schemacs" as well, and she very kindly agreed to allow us to use the name Schemacs, as was discussed in [issue 10 of guenchi/Schemacs](https://github.com/guenchi/Schemacs/issues/10).

# README

## Project Goals

Although this project is still incomplete and experimental, the goals of this project are to construct a Scheme app platform similar to Emacs, not just in the UI/UX, but also to be backward compatible (to the greatest degree possible) with GNU Emacs by implementing an Emacs Lisp interpreter as well.

- written in [**portable**](https://codeberg.org/ramin_hal9001/schemacs/wiki/Portability.md) R7RS Scheme, should run on any compliant Scheme implementation.
- able to run your `init.el`, run Emacs software pulled from ELPA.
- use Emacs Regression Tests (ERT) from GNU Emacs to ensure compatibility.
- encourage the use of the Scheme programming language to develop apps and text editing workflows.

### Sub-goals

- contribute patches upstream to the Guile Scheme Emacs Lisp compiler
- provide a cross-platform GUI library like [Racket/GUI](https://docs.racket-lang.org/gui/) or [McCLIM](https://mcclim.common-lisp.dev/)
- be able to develop Schemacs from within it's own editor, create pull requests in Git.

## How to help contribute code

### Code of Conduct

We respectfully ask all contributors to this project adhere to the principles stated in the [Code of Conduct (CoC)](https://emacsconf.org/2024/talks/gypsum/), so please be sure you read and understand this agreement before asking to contribute. The CoC is currently based on the [Contributor Covenant 3.0 Code of Conduct](https://www.contributor-covenant.org/version/3/0/code_of_conduct/).

### Project guidelines

The goal of this project is to have an Emacs-like app platform (including a text editor) that is backward compatible with GNU Emacs that runs on any R7RS-compliant Scheme implementation on any operating system. So please keep in mind the following guidelines:

- **Code should be [portable](https://codeberg.org/ramin_hal9001/schemacs/wiki/Portability.md).** As much of this project as possible should be written in platform-independent, portable, R7RS "small" standard-compliant Scheme. See the document titled "[How to make it More portable](https://codeberg.org/ramin_hal9001/schemacs/wiki/Portability.md)" for more information about this.

- **Multiple front-end GUI frameworks are encouraged!** GUI and platform-dependent code should be interfaced to rest of the project through a well-defined *parameterizable* interface.

- **Developing new editor features in Scheme is preferred over Emacs Lisp.** Backward compatibility with GNU Emacs is a goal of this project, but Emacs Lisp should otherwise be avoided. The Emacs Lisp interpreter is only to allow GNU Emacs users to run their configuration files without modification. New features of this software should be written in Scheme.
