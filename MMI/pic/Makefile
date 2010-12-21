#FILES := $(ls -1 *.svg)
#PDF	:= $(patsubst %.svg, %.pdf, $(echo *.svg))
SVG=$(shell ls -1 *.svg)
PDF=$(SVG:%.svg=%.pdf)
PNG=$(SVG:%.svg=%.png)
EPS=$(SVG:%.svg=%.eps)
DVI=$(SVG:%.svg=%.dvi)
INKSCAPE = /Applications/Inkscape.app/Contents/Resources/bin/inkscape

pdf : $(PDF)
png : $(PNG)
eps : $(EPS)
dvi : $(DVI)

%.pdf : %.svg
	@echo "pdf from " $<
	@ $(INKSCAPE) $< --export-pdf=$@ 2> /dev/null

%.png : %.svg
	@echo "png from " $<
	@ $(INKSCAPE) $< --export-png=$@ --export-width=1200 2> /dev/null

%.eps : %.svg
	@echo "eps from " $<
	@ $(INKSCAPE) $< --export-eps=$@ 2> /dev/null

%.dvi : %.svg
	@echo "dvi from " $<
	@ $(INKSCAPE) $< --export-dvi=$@ 2> /dev/null
