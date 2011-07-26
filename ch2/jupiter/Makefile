package = jupiter
version = 1.0
tarname = $(package)
distdir = $(tarname)-$(version)
prefix = /usr/local
export prefix

all clean install jupiter:
	cd src && $(MAKE) $@

dist: $(distdir).tar.gz

$(distdir).tar.gz: $(distdir)
	tar chof - $(distdir) | gzip -9 -c > $@
	rm -rf $(distdir)

$(distdir):
	mkdir -p $(distdir)/src
	cp Makefile $(distdir)
	cp src/Makefile $(distdir)/src
	cp src/main.c $(distdir)/src

.PHONY: all clean dist install
