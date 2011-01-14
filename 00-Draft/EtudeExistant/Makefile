LATEX=latex -shell-escape
PDF=pdflatex -shell-escape
DVIPDF=dvipdf

RM=rm -rfv
MV=mv -v
ECHO=@echo

all: pdf 

re: clean all

dvi:
	${ECHO} "	*** Generating dvi file... ***"
	${LATEX} *.tex
	if test -e *.toc;\
	then ${LATEX} *.tex;\
	fi
	${ECHO} "	*** dvi file generated. ***"

pdf:
	${ECHO} "	*** Generating pdf file... ***"
	${PDF} *.tex
	if test -e *.toc;\
	then ${PDF} *.tex;\
	fi
	${ECHO} "	*** pdf file generated. ***"

dvipdf: dvi
	${ECHO} "	*** Generating pdf file... ***"
	${DVIPDF} *.dvi
	${ECHO} "	*** pdf file generated. ***"
	
cleanall: clean
	${ECHO} "	*** Cleaning... ***"
	${RM} *.{dvi,pdf}
	${ECHO} "	*** Done. ***"

clean:
	${ECHO} "	*** Cleaning all... ***"
	${RM} *.{aux,log,toc,out,pyg,glo,ist}
	${ECHO} "	*** Done. ***"

