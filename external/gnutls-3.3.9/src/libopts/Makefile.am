## LIBOPTS Makefile
MAINTAINERCLEANFILES    = Makefile.in

noinst_LTLIBRARIES      = libopts.la
 
libopts_la_SOURCES      = libopts.c
libopts_la_CPPFLAGS     = -I$(top_srcdir)
libopts_la_LIBADD       = $(LTLIBINTL)
EXTRA_DIST		=
BUILT_SOURCES		=
MOSTLYCLEANFILES	=

+_NORETURN_H=$(srcdir)/compat/_Noreturn.h
EXTRA_DIST += $(srcdir)/compat/_Noreturn.h
BUILT_SOURCES += $(STDNORETURN_H)
if GL_GENERATE_STDNORETURN_H
stdnoreturn.h: stdnoreturn.in.h $(top_builddir)/config.status $(_NORETURN_H)
	$(AM_V_GEN)rm -f $@-t $@ && \
	{ echo '/* DO NOT EDIT! GENERATED AUTOMATICALLY! */' && \
	  sed -e '/definition of _Noreturn/r $(_NORETURN_H)' \
              < $(srcdir)/stdnoreturn.in.h; \
	} > $@-t && \
	mv $@-t $@
else
stdnoreturn.h: $(top_builddir)/config.status
	rm -f $@
endif
MOSTLYCLEANFILES += stdnoreturn.h stdnoreturn.h-t
EXTRA_DIST += stdnoreturn.in.h
 
EXTRA_DIST += \
    COPYING.gplv3           COPYING.lgplv3          COPYING.mbsd  \
    MakeDefs.inc            README                  ag-char-map.h  \
    alias.c                 ao-strs.c               ao-strs.h  \
    autoopts/options.h      autoopts/project.h      autoopts/usage-txt.h  \
    autoopts.c              autoopts.h              boolean.c  \
    check.c                 compat/strdup.c         compat/snprintf.c  \
    compat/compat.h         compat/_Noreturn.h      compat/pathfind.c  \
    compat/windows-config.h compat/strchr.c         configfile.c  \
    cook.c                  enum.c                  env.c  \
    file.c                  find.c                  genshell.c  \
    genshell.h              gettext.h               init.c  \
    intprops.h              load.c                  m4/libopts.m4  \
    m4/liboptschk.m4        m4/stdnoreturn.m4       makeshell.c  \
    nested.c                numeric.c               option-value-type.c  \
    option-value-type.h     option-xat-attribute.c  option-xat-attribute.h  \
    parse-duration.c        parse-duration.h        pgusage.c  \
    proto.h                 putshell.c              reset.c  \
    restore.c               save.c                  sort.c  \
    stack.c                 stdnoreturn.in.h        streqvcmp.c  \
    text_mmap.c             time.c                  tokenize.c  \
    usage.c                 version.c
