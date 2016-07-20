all: thesis.pdf

# LaTeX must be run multiple times to get references and glossaries right:
# http://tex.stackexchange.com/questions/74163/glossaries-issue-wrong-pagenumber-for-book-and-memoir
# latex latex makeglossary bibtex latex latex makeglossary latex 
thesis.pdf: thesis.tex $(wildcard *.tex) bibliography.bib
	pdflatex $<
	pdflatex $<
	makeglossaries thesis
	bibtex thesis
	pdflatex $<
	pdflatex $<
	makeglossaries thesis
	pdflatex $<

clean:
	rm -f *.log *.dvi *.aux *.toc *.lof *.lot *.out *.bbl *.blg
	rm -f thesis.pdf

purge:
	rm -f *.log *.dvi *.aux *.toc *.lof *.lot *.out *.bbl *.blg *._aux *._log *.nav *.synctex.gz *.project.vim .tmp/* *-blx.bib *.run.xml *.snm *.bcf
	rm -f thesis.pdf
