default:
	make print

print:
	pdflatex --halt-on-error printa.tex > /dev/null
	pdflatex --halt-on-error print-2x2.tex > /dev/null

thumb:
	inkscape -f piraten.svg 	\
		--export-width=650 	\
		--export-png=/tmp/piraten.png

	convert /tmp/piraten.png 	\
		-background white 	\
		-flatten 		\
		-gravity center 	\
		-extent 662x770 	\
		-border 1x1 		\
		-bordercolor "#AAA" 	\
		./thumb.png

	rm /tmp/piraten.png
