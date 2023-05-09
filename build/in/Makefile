SRC := $(wildcard ./*.m4d)
HTML    := $(SRC:.m4d=.md)

.PHONY: all

all: $(HTML)

$(HTML): %.md: %.m4d
	awk -f ../scripts/gawkt.awk $^ | m4 -R ../scripts/def.m4f > ../out/$(notdir $@)
	#touch $@

