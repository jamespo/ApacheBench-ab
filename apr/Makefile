# APR=apr-1.5.2
# APRUTIL=apr-util-1.5.4
APR=apr-1.7.5
APRUTIL=apr-util-1.6.3
APRREPO=https://archive.apache.org/dist/apr

all:$(APR) $(APRUTIL) buildapr

$(APR):
	wget $(APRREPO)/$(APR).tar.gz
	tar -xf $(APR).tar.gz
$(APRUTIL):
	wget $(APRREPO)/$(APRUTIL).tar.gz
	tar -xf $(APRUTIL).tar.gz

buildapr:
	cp Makefile_apr $(APR)
	make -C $(APR) -f Makefile_apr	
	cp Makefile_aprutil $(APRUTIL)
	make -C $(APRUTIL) -f Makefile_aprutil

clean:
	rm -rf apr-*
	rm -rf aprutil-*
