SUBDIRS = src

pixmaps= \
  src/pixmaps/Build.xpm  \
  src/pixmaps/donate.xpm  \
  src/pixmaps/future.xpm  \
  src/pixmaps/Gen.xpm   \
  src/pixmaps/interface.xpm  \
  src/pixmaps/load.xpm \
  src/pixmaps/preference.xpm  \
  src/pixmaps/reset.xpm \
  src/pixmaps/save.xpm \
  src/pixmaps/save16.xpm  \
  src/pixmaps/send.xpm \
  src/pixmaps/X.xpm

pixmapdir=$(pkgdatadir)/pixmaps
pixmap_DATA=$(pixmaps)

# Include the dev and pixmaps in the distribution (make dist)
EXTRA_DIST=dev src/pixmaps

## Define an independent executable script for inclusion in the distribution
## archive. It will not be installed on an end user's system, however.
dist_noinst_SCRIPTS = autogen.sh
