PORTNAME=        fna3d
DISTVERSION=     21.11
CATEGORIES=      graphics
LICENSE=         ZLIB

USE_GITHUB=      yes
GH_ACCOUNT=      FNA-XNA
GH_PROJECT=      FNA3D
GH_TUPLE=        icculus:mojoshader:7d5cc1c:mojoshader/MojoShader

USES=            cmake sdl
USE_SDL=         sdl2

BUILD_DEPENDS=   ${LOCALBASE}/include/vulkan/vulkan.h:graphics/vulkan-headers

CFLAGS+=         -I${LOCALBASE}/include

do-install:
	${CP} ${BUILD_WRKSRC}/libFNA3D.so.0.${DISTVERSION} ${STAGEDIR}${PREFIX}/lib/

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/lib/libFNA3D.so.0.${DISTVERSION}
	${RLN} ${STAGEDIR}${PREFIX}/lib/libFNA3D.so.0.${DISTVERSION} ${STAGEDIR}${PREFIX}/lib/libFNA3D.so
	${RLN} ${STAGEDIR}${PREFIX}/lib/libFNA3D.so.0.${DISTVERSION} ${STAGEDIR}${PREFIX}/lib/libFNA3D.so.0

PLIST_FILES=     lib/libFNA3D.so.0.${DISTVERSION} \
                 lib/libFNA3D.so.0 \
                 lib/libFNA3D.so

.include <bsd.port.mk>
