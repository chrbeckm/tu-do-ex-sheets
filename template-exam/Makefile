TeXOptions = \
  -lualatex \
  --output-directory=build \
  --interaction=nonstopmode \
  --halt-on-error

all: build/exam.pdf build/solution.pdf

build/exam.pdf: FORCE | build
	latexmk $(TeXOptions) exam.tex

preview: FORCE | build
	latexmk -pvc $(TeXOptions) exam.tex

build/solution.pdf: FORCE | build
	latexmk $(TeXOptions) --jobname=solution exam.tex

preview-solution: FORCE | build
	latexmk -pvc $(TeXOptions) --jobname=solution exam.tex

FORCE:

build:
	mkdir -p build

clean:
	rm -rf build


.PHONY: all clean FORCE
