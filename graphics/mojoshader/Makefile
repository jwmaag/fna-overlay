
PORTNAME=        mojoshader
PORTVERSION=     1305         # changeset
CATEGORIES=      graphics
LICENSE=         ZLIB

USE_GITHUB=      yes
GH_ACCOUNT=      FNA-XNA
GH_PROJECT=      MojoShader
GH_TAGNAME=      10bbf0e

BUILD_DEPENDS=   re2c:devel/re2c \
	${LOCALBASE}/include/vulkan/vulkan.h:devel/vulkan-headers

USES=            cmake sdl
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
