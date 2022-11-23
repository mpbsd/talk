TEX_ENGINE = xelatex
BIB_ENGINE = bibtex
OPR_SYSTEM = $(shell uname -s)

ifeq ($(OPR_SYSTEM), Darwin)
	DOC_VIEWER = open -a Preview
else
	DOC_VIEWER = zathura
endif

draft:
	$(TEX_ENGINE) poesia
	$(DOC_VIEWER) poesia.pdf

clean:
	find . -type f -name poesia.aux | xargs rm -rf
	find . -type f -name poesia.idx | xargs rm -rf
	find . -type f -name poesia.log | xargs rm -rf
	find . -type f -name poesia.pdf | xargs rm -rf

.PHONY: draft clean
