SHELL = /bin/bash

.PHONY: clean


default:
	pdflatex main

all: main.tex
	pdflatex main
	bibtex main
	pdflatex main
	pdflatex main

clean:
	rm -f main.{aux,out,ind,ilg,log,lot,lof,bbl,blg,dvi,tar,tgz,toc,idx,tmp,ps,pdf,*~} main.{aux,out,ind,ilg,log,lot,lof,bbl,blg,dvi,tar,tgz,toc,idx,tmp,ps,pdf,*~} master.{aux,out,ind,ilg,log,lot,lof,bbl,blg,dvi,tar,tgz,toc,idx,tmp,ps,pdf,*~} *.tex~ references.*~ Makefile~

archive:
	tar -cf main.tar `ls *.tex *.txt *.cls *.sty *.bib  Makefile`
	gzip -9 main.tar
	mv main.tar.gz main.tgz

