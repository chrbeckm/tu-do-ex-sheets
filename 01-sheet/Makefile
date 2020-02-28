Nr = 01
TeXOptions = \
  -lualatex \
  --output-directory=build \
  --interaction=nonstopmode \
  --halt-on-error

all: build/$(Nr)-sheet.pdf build/$(Nr)-solution.pdf

build/$(Nr)-sheet.pdf: FORCE | build
	latexmk $(TeXOptions) $(Nr)-sheet.tex

preview: FORCE | build
	latexmk -pvc $(TeXOptions) $(Nr)-sheet.tex

build/$(Nr)-solution.pdf: FORCE | build
	latexmk $(TeXOptions) --jobname=solution $(Nr)-sheet.tex
	cp build/solution.pdf build/$(Nr)-solution.pdf

preview-solution: FORCE | build
	latexmk -pvc $(TeXOptions) --jobname=solution $(Nr)-sheet.tex

FORCE:

build:
	mkdir -p build

clean:
	rm -rf build


.PHONY: all clean FORCE
