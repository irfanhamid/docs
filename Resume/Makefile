SOURCES=Hamid_En.texinfo\
	Makefile

BASE=Hamid_En

all: $(BASE).dvi

pdf: $(BASE).pdf

ps: $(BASE).ps

$(BASE).dvi: $(SOURCES)
	texi2dvi $(BASE).texinfo

$(BASE).pdf: $(SOURCES)
	texi2pdf $(BASE).texinfo

$(BASE).ps: $(SOURCES)
	texi2ps $(BASE).texinfo

html: $(SOURCES)
	makeinfo --html --css-include=style.css $(BASE).texinfo

clean:
	rm -rf *~ *.pdf *.ps *.dvi *# *.log *.fn *.toc *.vr *.cp *.aux *.tp *.ky *.pg 
