figdir = figures
docname = gnucash-guide
lang = zh-CN
fopconfig = fop.xconf
omffile = $(docname)-zh-CN.omf
entities = \
	legal.xml \
	ch_oview.xml \
	ch_basics.xml \
	ch_accts.xml \
	ch_txns.xml \
	ch_cbook.xml \
	ch_cc.xml \
	ch_python_bindings.xml 
DISTCLEANFILES =  $(docname)-zh-CN.omf.out mincho.xml gothic.xml $(fopconfig)
CLEANFILES =  $(DISTCLEANFILES)
FOPFLAGS = -l $(lang) -c $(fopconfig)
XSLTFLAGS_FO= --stringparam paper.type A4
if GNC_WINDOWS
include $(top_srcdir)/chm.make
else
include $(top_srcdir)/xmldocs.make
include $(top_srcdir)/pdf.make
include $(top_srcdir)/epub.make
if WITH_MOBI
include $(top_srcdir)/mobi.make
endif
endif
