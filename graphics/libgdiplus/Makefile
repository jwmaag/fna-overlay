PORTNAME=      libgdiplus
DISTVERSION=   6.0.5
CATEGORIES=    graphics
MAINTAINER=    jwmaag@gmail.com
COMMENT=       GDI+ implementation for mono

USE_GITHUB=    yes
GH_ACCOUNT=    mono
GH_PROJECT=    libgdiplus

LIB_DEPENDS=   libcairo.so:graphics/cairo \
	libfontconfig.so:x11-fonts/fontconfig \
	libfreetype.so:print/freetype2 \
	libtiff.so:graphics/tiff \
	libpng16.so:graphics/png \
	libexif.so:graphics/libexif \
	libgif.so:graphics/giflib

USES=          autoreconf gmake libtool pkgconfig gnome \
			   gettext-runtime xorg

USE_GNOME=     glib20
USE_XORG=      x11

GNU_CONFIGURE= yes

INSTALL_TARGET= install-strip

.include <bsd.port.mk>
