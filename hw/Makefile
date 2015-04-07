all: hw1.html

.PHONY: all clean

%.html : %.md
	pandoc $^ -o $@

clean:
	rm -f hw1.html
