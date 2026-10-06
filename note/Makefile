LATEXMK ?= latexmk
LATEXFLAGS = -silent -pdf -interaction=nonstopmode -halt-on-error

.PHONY: all
all: lecture.pdf

# The lecture notes before the midterm are one self-contained file.
lecture.pdf: lecture.tex
	$(LATEXMK) $(LATEXFLAGS) -outdir=.build/lecture $<
	cp .build/lecture/lecture.pdf lecture.pdf

# When the commented source lecture-src.tex is present, lecture.tex is generated from it
# without the comment lines.
ifneq ($(wildcard lecture-src.tex),)
lecture.tex: lecture-src.tex
	sed '/^[[:space:]]*%/d' $< | cat -s > $@
endif
