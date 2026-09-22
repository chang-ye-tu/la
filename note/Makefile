LATEXMK ?= latexmk
LATEXFLAGS = -silent -pdf -interaction=nonstopmode -halt-on-error
UNIT_MASTERS := $(wildcard unit[0-9][0-9].tex)
UNIT_PDFS := $(UNIT_MASTERS:.tex=.pdf)

.PHONY: all
all: $(UNIT_PDFS)

# Cross-unit references require the earlier auxiliary files even when a
# checkout already contains the published PDFs. Build in teaching order;
# grouped outputs prevent two requests from compiling the same unit.
define UNIT_RULE
$(1).pdf .build/$(1)/$(1).aux &: $(1).tex unit-preamble.tex $(wildcard $(1)-*.tex) $(2)
	$$(LATEXMK) $$(LATEXFLAGS) -outdir=.build/$(1) $$<
	cp .build/$(1)/$(1).pdf $(1).pdf
endef

PREVIOUS_UNITS :=
$(foreach unit,$(basename $(UNIT_MASTERS)),\
  $(eval $(call UNIT_RULE,$(unit),$(foreach prior,$(PREVIOUS_UNITS),$(prior).pdf .build/$(prior)/$(prior).aux)))\
  $(eval PREVIOUS_UNITS += $(unit)))
