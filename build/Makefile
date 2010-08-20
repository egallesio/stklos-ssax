COMMON = ssax-error.stk ssax-prelude.stk ssax-core.stk
SRC    = $(COMMON) ssax.stk 
TSRC   = $(COMMON) ssax-test.stk ssax-test-body.stk

EXE    = make-source 

SFLAGS = -c 


all: $(EXE) ../ssax-core.stk

make-source: make-source.stk
	stklos-compile -o make-source make-source.stk

#ssax.ostk: $(SRC)
#	stklos-compile $(SFLAGS) -o ssax.ostk ssax.stk 

ssax-test: $(TSRC)
	stklos-compile $(SFLAGS) -o ssax-test ssax-test.stk

../ssax-core.stk: SSAX.scm make-source
	make-source SSAX.scm ../ssax-core.stk ../test/ssax-test-body.stk

clean:
	rm -f *~ $(EXE) 

distclean: clean
