#
#	@(#)Makefile	1.10	94/06/18
#
DEST	      = $(DEST_LIB)/bmac

MAKEFILE      = Makefile

PRINT	      = vtroff

BIBSRCS	      = bib.astro \
		bib.compsurv \
		bib.foot \
		bib.hnf \
		bib.jrnl \
		bib.lib \
		bib.list \
		bib.llist \
		bib.opena \
		bib.openn \
		bib.spe \
		bib.spe2 \
		bib.stda \
		bib.stdafull \
		bib.stdn \
		bib.stdsn \
		bib.supn \
		bibinc.names \
		bibmac.me \
		bmac.open \
		bmac.std \
		common \
		macros.me \
		Makefile.e.g.

BIBINCS	      = bibinc.fullnames \
		bibinc.shortnames \
		bibinc.publishers \
		tibinc.fullnames \
		tibinc.shortnames

.PHONY: depend install clean all

all:;

clean:;

depend:;	@mkmf -f $(MAKEFILE)

install:	${BIBINCS}
		-mkdir $(DEST)
		-mkdir $(DEST)/bibmacs
		-mkdir $(DEST)/tibmacs
		cp bibinc.fullnames $(DEST)/bibmacs
		cp bibinc.shortnames $(DEST)/bibmacs
		cp bibinc.publishers $(DEST)/bibmacs
		cp tibinc.fullnames $(DEST)/tibmacs/bibinc.fullnames
		cp tibinc.shortnames $(DEST)/tibmacs/bibinc.shortnames
		cp bibinc.fulllocal $(DEST)/bibmacs
		cp bibinc.shortlocal $(DEST)/bibmacs
		cp bibinc.fulllocal $(DEST)/tibmacs
		cp bibinc.shortlocal $(DEST)/tibmacs
		@echo Installing in $(DEST)
		csh -f ./Install $(DEST) $(BIBSRCS) ;

$(DEST):
		mkdir $(DEST)

bibinc.shortnames bibinc.fullnames: bibinc.names
	bibinc <bibinc.names

tibinc.fullnames tibinc.shortnames: bibinc.names
	bibinc -Tib -Tex <bibinc.names
	
update:;
