DOC = apostila
PARTES := $(wildcard ./partes/*)

.PHONY: all clean

all: $(DOC).pdf clean

$(DOC).pdf: $(DOC).Rnw $(PARTES)
	Rscript -e "knitr::knit2pdf('$<', compiler = 'xelatex', encoding = 'UTF-8')"

clean:
	rm -rf ./figure $(addprefix $(DOC), .aux .bbl .blg .log .out .tex .toc) *.tex
