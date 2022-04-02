FILE1=req
FILE2=reqd

ping:$(FILE1).png

$(FILE1).dvi:$(FILE1).tex
	platex $<

$(FILE1).pdf:$(FILE1).dvi
	dvipdfmx $<

$(FILE1).png:$(FILE1).pdf
	convert -density 400 $< \( +clone -alpha opaque -fill white -colorize 100% \) +swap -geometry +0+0 -compose Over -composite -alpha off $(FILE1).png

pdf:$(FILE2).pdf

$(FILE2).dvi:$(FILE2).tex
	platex $<

$(FILE2).pdf:$(FILE2).dvi
	dvipdfmx $<

	
