PORTNAME=        hashlink
DISTVERSION=     1.11
CATEGORIES=      lang
MAINTAINER=      jwmaag@gmail.com

USE_GITHUB=      yes
GH_ACCOUNT=      HaxeFoundation
GH_PROJECT=      hashlink


LIB_DEPENDS=     libpng16.so:graphics/png \
	libturbojpeg.so:graphics/libjpeg-turbo \
	libvorbisfile.so:audio/libvorbis \
	libmbedtls.so:security/mbedtls \
	libmbedx509.so:security/mbedtls \
	libmbedcrypto.so:security/mbedtls \
	libuv.so:devel/libuv

USES=            gmake sdl openal
USE_SDL=         sdl2

CFLAGS+=         -I${LOCALBASE}/include
MAKE_ARGS=        LIBFLAGS="-L${LOCALBASE}/lib" INSTALL_DIR=${STAGEDIR}${PREFIX}

# INSTALL_TARGET=   install-strip
#
post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/lib/*.hdll
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/lib/*.so
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/hl

.include <bsd.port.mk>
