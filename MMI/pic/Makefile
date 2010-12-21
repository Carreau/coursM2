#FILES := $(ls -1 *.svg)
#PDF	:= $(patsubst %.svg, %.pdf, $(echo *.svg))
SVG=$(shell ls -1 *.svg)
PDF=$(SVG:%.svg=%.pdf)
PNG=$(SVG:%.svg=%.png)
INKSCAPE = /Applications/Inkscape.app/Contents/Resources/bin/inkscape

pdf : $(PDF)
png : $(PNG)

%.pdf : %.svg
	@echo "pdf from " $<
	@ $(INKSCAPE) $< --export-pdf=$@ 2> /dev/null


%.png : %.svg
	@echo "png from " $<
	@ $(INKSCAPE) $< --export-png=$@ 2> /dev/null
