MODULE_TOPDIR = ..

SUBDIRS = timer g.html2man

include $(MODULE_TOPDIR)/include/Make/Dir.make
include $(MODULE_TOPDIR)/include/Make/Compile.make

default: parsubdirs $(UTILSDIR)/mkhtml.py \
	$(UTILSDIR)/generate_last_commit_file.py \
	$(UTILSDIR)/g.echo$(EXE)

$(UTILSDIR)/mkhtml.py: mkhtml.py
	$(INSTALL) $< $@

$(UTILSDIR)/generate_last_commit_file.py: generate_last_commit_file.py
	$(INSTALL) $< $@

$(UTILSDIR)/g.echo$(EXE): $(OBJDIR)/g.echo.o
	$(call linker_base,$(LINK),$(LDFLAGS) $(EXTRA_LDFLAGS),$(MANIFEST_OBJ))
