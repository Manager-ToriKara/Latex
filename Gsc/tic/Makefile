FILE=tic

all:$(FILE).png

$(FILE).dvi:$(FILE).tex
	platex $<

$(FILE).pdf:$(FILE).dvi
	dvipdfmx $<

$(FILE).png:$(FILE).pdf
	convert -density 400 $< \( +clone -alpha opaque -fill white -colorize 100% \) +swap -geometry +0+0 -compose Over -composite -alpha off $(FILE).png
