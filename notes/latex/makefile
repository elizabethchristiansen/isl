LATEX := $(shell find sections -name '*.tex')
INCLUDES := $(shell find includes -name '*.tex')
IMAGES := $(shell find images -name '*.png')
IMAGES_PDF := $(shell find images -name '*.pdf')

notes.pdf: main.tex $(INCLUDES) $(LATEX) $(IMAGES) $(IMAGES_PDF)
	latexmk --pdf $<
	@mv main.pdf ../notes.pdf

open:
	@open -n ../notes.pdf
	
clean:
	- find . -type f -not \( -name '*tex' -or -name 'makefile' -or -name '*png' -or -name '*pdf' -or -name '*bib' \) -delete
