FILES = $(patsubst %.md,%.docx,$(wildcard *.md))
FILES += $(patsubst %.md,%.pdf,$(wildcard *.md))

%.docx: %.md
	pandoc $< -o $@

%.pdf: %.md
	pandoc $< --pdf-engine=xelatex -V mainfont="DejaVu Sans" -o $@

all: $(FILES)

clean:
	rm -f *.docx *.pdf
