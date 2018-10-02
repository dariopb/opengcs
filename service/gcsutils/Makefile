.PHONY: clean test-all test-exportSandbox

TESTDIR=test
INPUTPATH=$(TESTDIR)/input.tar
VHDPATH=$(TESTDIR)/input.vhd
OUTPUTPATH=$(TESTDIR)/output.tar
TESTFOLDER=$(TESTDIR)/folder

test-all: test-exportSandbox

test-exportSandbox:
	mkdir -p $(TESTFOLDER)/upper
	tar xf $(INPUTPATH) -C $(TESTFOLDER)/upper
	$(BINDIR)/exportSandbox -path $(TESTFOLDER) > $(OUTPUTPATH)
	cmp $(INPUTPATH) $(OUTPUTPATH)
	rm -rf $(OUTPUTPATH) $(TESTFOLDER)
