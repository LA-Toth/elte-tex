.PHONY:  all build edit log viewpdf silent make pdf emacs-x emacs e ex
NAME=$(notdir $(shell pwd))
FILE ?= ${NAME}.tex

all:	build
build:	$(NAME).tex
	pslatex ${NAME}.tex
	pdflatex ${NAME}.tex
edit:
	mcedit  ${FILE}
emacs-x:
	emacs ${FILE} &
emacs:
	@emacs -nw ${FILE}
e: emacs
ex: emacs-x
log:
	@mcview ${NAME}.log
viewpdf:
	@acroread $(NAME).pdf
silent:	$(NAME).tex
	@pdflatex ${NAME}.tex >/dev/null 2>&1
dvi:
	@pslatex ${NAME}.tex
make:
	mcedit Makefile
pdf: silent viewpdf
