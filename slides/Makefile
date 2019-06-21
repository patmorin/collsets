
name=collsets

texsource=slides-socg.tex 

slides-socg.pdf : $(texsource) figs/ images/
	make -C figs
	latexmk -pdf $(texsource)

reset : clean $(name).pdf

clean :
	rm -f $(texsource).pdf

install: slides-socg.pdf
	scp $< cglab.ca:public_html/publications/drafts/$(name)/slides-socg.pdf
