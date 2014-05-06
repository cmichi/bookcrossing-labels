all:
	make print
	make thumb

print:
	pdflatex --halt-on-error printa.tex > /dev/null
	pdflatex --halt-on-error print-2x2.tex > /dev/null

print-2x3:
	pdflatex --halt-on-error printa-2x3.tex > /dev/null
	pdflatex --halt-on-error print-2x3.tex > /dev/null

thumb:
	inkscape -f piraten.svg 	\
		--export-width=504 	\
		--export-height=588 	\
		--export-png=/tmp/piraten.png

	convert /tmp/piraten.png 	\
		-background white 	\
		-flatten 		\
		-gravity center 	\
		-extent 514x598 	\
		-border 1x1 		\
		-bordercolor "#AAA" 	\
		./thumb.png

	rm /tmp/piraten.png

	convert ./print-2x2.pdf 	\
		-background white 	\
		-flatten 		\
		-resize 504x713		\
		-gravity center 	\
		-extent 514x723 	\
		-border 1x1 		\
		-bordercolor "#AAA" 	\
		./thumb-2x2.png
