# PFLAGS=	--filter pandoc-minted

%.pdf: %.tex
	latexmk -xelatex $< -shell-escape

%.tex: %.md
	pandoc $< \
		-s -o $@ \
		--from markdown \
		--to beamer \
		${PFLAGS}
