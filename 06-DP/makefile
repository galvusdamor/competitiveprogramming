THIS_DIR := $(dir $(abspath $(lastword $(MAKEFILE_LIST))))
THIS_UB := $(lastword $(subst /, ,$(THIS_DIR)))
THIS_TEX := $(shell ls *tex)

all: handout regular
	
	make clean

handout: $(THIS_TEX)
	xelatex -shell-escape -jobname $(THIS_UB)-Handout \\def\\handoutstyle{handout}\\input{$(THIS_TEX)}
	xelatex -shell-escape -jobname $(THIS_UB)-Handout \\def\\handoutstyle{handout}\\input{$(THIS_TEX)}
	xelatex -shell-escape -jobname $(THIS_UB)-Handout \\def\\handoutstyle{handout}\\input{$(THIS_TEX)}

regular: $(THIS_TEX)
	xelatex -shell-escape -jobname $(THIS_UB) \\def\\handoutstyle{}\\input{$(THIS_TEX)}
	xelatex -shell-escape -jobname $(THIS_UB) \\def\\handoutstyle{}\\input{$(THIS_TEX)}
	xelatex -shell-escape -jobname $(THIS_UB) \\def\\handoutstyle{}\\input{$(THIS_TEX)}

clean:
	rm *.aux *.log *.nav *.out *.snm *.toc *.vrb

