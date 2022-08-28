TEX := hello.tex
PDF := $(TEX:%.tex=%.pdf)
DEP := $(TEX:%.tex=%.d)

all: $(PDF)

-include $(DEP)

%.pdf: %.tex
	latexmk -pdf -M -MF $(DEP) $<

clean:
	rm -f *.{dvi,bbl,blg,aux,fls,log,fdb_latexmk,out,def,ques,listing,pdf,toc,loa} $(DEP)
