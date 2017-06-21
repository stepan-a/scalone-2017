LATEX=pdflatex

.PHONY=clean clean-all

all: slides.pdf clean

slides.pdf: slides.tex
	while ($(LATEX) slides.tex ; \
	grep -q "Rerun to get cross" slides.log ) do true ; \
	done

clean:
	rm -f slides.aux  slides.log  slides.nav  slides.out slides.snm  slides.toc
	rm -rf auto

clean-all: clean
	rm slides.pdf
