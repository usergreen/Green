VERSION = 3.4
FTPDIR = /proj/itl/www/div826/subject/expect/stopwatch

install:
	# There's nothing to install!  Simply run stopwatch!

stopwatch-$(VERSION).tar:
	rm -f ../stopwatch-$(VERSION)
	ln -s `pwd` ../stopwatch-$(VERSION)
	cd ..;tar cvfh $@ `pubfile stopwatch-$(VERSION)`
	mv ../$@ .

stopwatch-$(VERSION).tar.gz:	stopwatch-$(VERSION).tar
	gzip -fc stopwatch-$(VERSION).tar > $@

stopwatch.tcl.html: stopwatch
	echo '<xmp>' > stopwatch.tcl.html
	cat stopwatch >> stopwatch.tcl.html
	echo '</xmp>' >> stopwatch.tcl.html

# make a release and install it on ftp server
ftp:	stopwatch-$(VERSION).tar.gz stopwatch.tcl.html
	cp index.html tclet.html README HISTORY stopwatch.tcl.html $(FTPDIR)
	cp stopwatch-$(VERSION).tar.gz $(FTPDIR)/stopwatch.tar.gz
	cp stopwatch $(FTPDIR)/stopwatch.tcl
	cp stopwatch1.2 $(FTPDIR)/
	cp stopwatch.gif $(FTPDIR)
	rm stopwatch-$(VERSION).tar*
	ls -l $(FTPDIR)/stopwatch.tar*
