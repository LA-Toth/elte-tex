.PHONY:  all build edit log viewpdf viewps silent make pdf
NAME=szoftszig
all:	build
build:	$(NAME).tex
	pslatex ${NAME}.tex
#	dvips ${NAME}.dvi
	pdflatex ${NAME}.tex
edit:
	mcedit  ${NAME}.tex
log:
	@mcview ${NAME}.log
viewpdf:
	@acroread $(NAME).pdf
viewps:
	@gv $(NAME).ps
silent:	$(NAME).tex
	@pslatex ${NAME}.tex >/dev/null 2>&1
#	dvips ${NAME}.dvi
	@pdflatex ${NAME}.tex >/dev/null 2>&1
make:
	mcedit Makefile
pdf: silent viewpdf
public:
	scp $(NAME).pdf p:public_html/
