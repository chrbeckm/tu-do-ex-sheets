# tu-do-ex-sheets
Repo for excercise sheet template, and for exam template with LaTeX.

The styling colors are according to TU Dortmund.

Not every comment is in english, sorry for that.
If there are challenges in understanding something, feel free to open an issue.

The sheets are with the `xSim`-package, the exam not,
the chosen method works better for me.


## Makefile
Use `make` to build both, sheet/exam and solution.
`make preview` for sheet/exam
`make preview-solution` for solution

## sheet-template
At the end of the header.tex is a definition for an exercise type.
If you need more, add them accordingly.
Line 78, might be interesting to change,
as well the defintion of the header in lines 149 - 161.

Everything else can be found in the `template.tex`.

## exam-template
Every relevant setting is marked with `%%% Settings`.
Add more exercises in the same way `Contents/A2.tex` is.

## References:
- https://github.com/MaxNoe/exsheets_template
- https://github.com/pep-dortmund/toolbox-workshop/tree/master/latex
