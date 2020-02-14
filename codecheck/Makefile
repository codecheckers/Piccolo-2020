## steps:
## make run
## make outputs
## make 


all: codecheck.pdf

piccolo2020-codecheck.html: piccolo2020-codecheck.Rmd summary_table.tex
	Rscript -e 'rmarkdown::render("$<")'

codecheck.pdf: piccolo2020-codecheck.Rmd summary_table.tex preamble.sty
	Rscript -e 'rmarkdown::render("$<", "pdf_document")'
	cp piccolo2020-codecheck.pdf codecheck.pdf

.PHONY: run clean

clean:
	rm -fr ../Figures piccolo2020-codecheck.html outputs

## This takes just a minute or so to re-run outputs

run:
	cd ..; Rscript -e 'rmarkdown::render("Analyze_Results.Rmd")'

