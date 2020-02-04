piccolo2020-codecheck.html: piccolo2020-codecheck.Rmd
	Rscript -e 'rmarkdown::render("$^")'


.PHONY: run clean

clean:
	rm -fr ../Figures piccolo2020-codecheck.html

## This takes just a minute or so to re-run outputs

run:
	cd ..; Rscript -e 'rmarkdown::render("Analyze_Results.Rmd")'


outputs: outputs/fig2.pdf \
         outputs/fig3.pdf \
	 outputs/fig4.pdf \
	 outputs/fig5.pdf \
	 outputs/fig6.pdf \
	 outputs/fig7.pdf


## Below is the mapping from the original data files to the figures
## in the manuscript.

outputs/fig2.pdf: ../Figures/Datasets_Basic_AUROC.pdf
	cp $^ $@

outputs/fig3.pdf: ../Figures/Predictions_Histograms.pdf
	cp $^ $@

outputs/fig4.pdf: ../Figures/Algorithms_ParamsImprovement_AUROC.pdf
	cp $^ $@

outputs/fig5.pdf: ../Figures/Algorithms_FSImprovement_AUROC.pdf
	cp $^ $@

outputs/fig6.pdf: ../Figures/FS_vs_CL.pdf
	cp $^ $@

outputs/fig7.pdf: ../Figures/FS_NumFeatures.pdf
	cp $^ $@
