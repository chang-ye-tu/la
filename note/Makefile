LATEXMK ?= latexmk
LATEXFLAGS = -silent -pdf -interaction=nonstopmode -halt-on-error

.PHONY: all
all: book.pdf

# The textbook is one self-contained file.
book.pdf: book.tex
	$(LATEXMK) $(LATEXFLAGS) -outdir=.build/book $<
	cp .build/book/book.pdf book.pdf

# When the commented source book-src.tex is present, book.tex is generated from it
# without the comment lines.
ifneq ($(wildcard book-src.tex),)
book.tex: book-src.tex
	sed '/^[[:space:]]*%/d' $< | cat -s > $@
endif
