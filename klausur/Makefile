TeXOptions = \
  -lualatex \
  --output-directory=build \
  --interaction=nonstopmode \
  --halt-on-error

all: build/Klausur-1.pdf build/Klausur-1-Loesung.pdf

build/Klausur-1.pdf: FORCE | build
	latexmk $(TeXOptions) Klausur-1.tex

preview: FORCE | build
	latexmk -pvc $(TeXOptions) Klausur-1.tex

build/Klausur-1-Loesung.pdf: FORCE | build
	latexmk $(TeXOptions) --jobname=solution Klausur-1.tex
	cp build/solution.pdf build/Klausur-1-Loesung.pdf

preview-solution: FORCE | build
	latexmk -pvc $(TeXOptions) --jobname=solution Klausur-1.tex

FORCE:

build:
	mkdir -p build

clean:
	rm -rf build


.PHONY: all clean FORCE
