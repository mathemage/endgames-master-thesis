all: presentation.pdf

# LaTeX must be run multiple times to get references right
presentation.pdf: presentation.tex $(wildcard *.tex) ../src/bibliography.bib
	xelatex $<
	bibtex presentation
	xelatex $<
	xelatex $<

clean:
	rm -f *.log *.dvi *.aux *.toc *.lof *.lot *.out *.bbl *.blg *._aux *._log *.nav *.synctex.gz *.project.vim .tmp/* *-blx.bib *.run.xml *.snm
	rm -f presentation.pdf
