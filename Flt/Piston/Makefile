all:piston.png

piston.dvi:piston.tex
	platex $<

piston.pdf:piston.dvi
	dvipdfmx $<

piston.png:piston.pdf
	convert -density 400 $< \( +clone -alpha opaque -fill white -colorize 100% \) +swap -geometry +0+0 -compose Over -composite -alpha off piston.png
