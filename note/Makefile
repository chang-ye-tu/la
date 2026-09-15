LATEXMK ?= latexmk
LATEXFLAGS = -silent -pdf -interaction=nonstopmode -halt-on-error
UNITS := unit01 unit02 unit03 unit04 unit05 unit06 unit07 unit08 unit09 unit10 unit11 unit12

.PHONY: all
all: $(addsuffix .pdf,$(UNITS)) unit01-2up.pdf

unit01-2up.pdf: unit01-2up.tex unit01.pdf
	$(LATEXMK) $(LATEXFLAGS) -outdir=.build/unit01-2up unit01-2up.tex
	cp .build/unit01-2up/unit01-2up.pdf $@

unit12.pdf: unit12-inequality-exercises.tex

unit%.pdf: unit%.tex unit%-content.tex unit%-exercises.tex unit-preamble.tex
	$(LATEXMK) $(LATEXFLAGS) -outdir=.build/unit$* unit$*.tex
	cp .build/unit$*/unit$*.pdf $@
