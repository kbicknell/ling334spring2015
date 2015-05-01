hwbase=hw1 hw2 hw3 project
hwhtml=$(addsuffix .html, $(hwbase))
all : $(hwhtml)

.PHONY : all clean

%.html : %.Rmd
	Rscript -e "require(rmarkdown); render('$<')"
hw3.html : hw3.Rmd hmm.svg
	Rscript -e "require(rmarkdown); render('$<')"
%.svg : %.pdf
	pdf2svg $^ $@
%.pdf : %.tex
	pdflatex $^

clean :
	rm -f $(hwhtml)
	rm -f hmm.pdf hmm.svg hmm.log hmm.aux
