PORTNAME=        mojoshader
# Previously this was a changeset value, but i believe the source has 
# been moved to github. there is no version right now so im just going to 
# bump the revision number for now
PORTVERSION=     1328         
CATEGORIES=      graphics
MAINTAINER=      jwmaag@gmail.com
LICENSE=         ZLIB

USE_GITHUB=      yes
GH_ACCOUNT=      icculus
GH_PROJECT=      mojoshader
GH_TAGNAME=      7d5cc1c

BUILD_DEPENDS=   re2c:devel/re2c \
	${LOCALBASE}/include/vulkan/vulkan.h:graphics/vulkan-headers

USES=            cmake sdl ninja
USE_SDL=         sdl2

CMAKE_ARGS=      -DBUILD_SHARED_LIBS=ON \
				 -DPROFILE_METAL=OFF \
				 -DFLIP_VIEWPORT=ON

CFLAGS+=         -I${LOCALBASE}/include

do-install:
	${CP} ${WRKSRC}/mojoshader*.h ${STAGEDIR}${PREFIX}/include/
	${CP} ${BUILD_WRKSRC}/libmojoshader.so ${STAGEDIR}${PREFIX}/lib/

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/lib/libmojoshader.so

.include <bsd.port.mk>
