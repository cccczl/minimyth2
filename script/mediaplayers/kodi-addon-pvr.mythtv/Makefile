
GARNAME      = pvr.mythtv
# branch nexus v20.3.0 @28.09.2022
GARVERSION   = e32e237d226481dd2ed907e56490dfb8f1724a38
CATEGORIES   = mediaplayers
MASTER_SITES = https://github.com/janbar/pvr.mythtv/archive/
DISTFILES    = $(GARVERSION).zip
LICENSE      = GPL2

DEPENDS = lang/c

WORKBLD = $(WORKSRC)_build

CONFIGURE_SCRIPTS = $(WORKBLD)/cmake
BUILD_SCRIPTS     = $(WORKBLD)/Makefile
INSTALL_SCRIPTS   = $(WORKBLD)/Makefile

CMAKE_CONFIGURE_ARGS = \
	-DCMAKE_VERBOSE_MAKEFILE="OFF" \
	-DCMAKE_BUILD_TYPE=Debug \
	-DCMAKE_INSTALL_PREFIX=$(datadir)/kodi/addons \
	-DCMAKE_MODULE_PATH=$(DESTDIR)$(datadir)/kodi/cmake \
	-DPACKAGE_ZIP=ON \
	-DKODI_INCLUDE_DIR=$(DESTDIR)$(includedir)/kodi \

include ../../gar.mk

clean-all:
	@rm -rf $(DESTDIR)$(datadir)/kodi/addons/pvr.mythtv
