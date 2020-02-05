## steps:
## make run
## make outputs
## make 

piccolo2020-codecheck.html: piccolo2020-codecheck.Rmd
	Rscript -e 'rmarkdown::render("$<")'

readme.pdf: piccolo2020-codecheck.Rmd
	Rscript -e 'rmarkdown::render("$<", "pdf_document")'
	cp piccolo2020-codecheck.pdf readme.pdf

.PHONY: run clean

clean:
	rm -fr ../Figures piccolo2020-codecheck.html outputs

## This takes just a minute or so to re-run outputs

run:
	cd ..; Rscript -e 'rmarkdown::render("Analyze_Results.Rmd")'

