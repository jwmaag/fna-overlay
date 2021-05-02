PORTNAME=        libtheorafile
PORTVERSION=     1.0.1
MAINTAINER=      jwmaag@gmail.com
CATEGORIES=      multimedia
LICENSE=         ZLIB

USE_GITHUB=      yes
GH_ACCOUNT=      FNA-XNA
GH_PROJECT=      Theorafile
GH_TAGNAME=      3f8bd6c

LIB_DEPENDS=     libogg.so:audio/libogg \
	libvorbis.so:audio/libvorbis \
	libtheoradec.so:multimedia/libtheora 

USES=            sdl gmake
USE_SDL=         sdl2

CFLAGS+=         -I${LOCALBASE}/include 

do-install:
	${CP} ${WRKSRC}/${PORTNAME}.so ${STAGEDIR}${PREFIX}/lib/
	${CP} ${WRKSRC}/theorafile.h ${STAGEDIR}${PREFIX}/include/

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/lib/${PORTNAME}.so

PLIST_FILES=      lib/${PORTNAME}.so \
				  include/theorafile.h

.include <bsd.port.mk>
