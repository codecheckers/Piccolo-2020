## steps:
## make run
## make outputs
## make 

piccolo2020-codecheck.html: piccolo2020-codecheck.Rmd
	Rscript -e 'rmarkdown::render("$<")'


.PHONY: run clean

clean:
	rm -fr ../Figures piccolo2020-codecheck.html outputs

## This takes just a minute or so to re-run outputs

run:
	cd ..; Rscript -e 'rmarkdown::render("Analyze_Results.Rmd")'

