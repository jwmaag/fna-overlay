PORTNAME=        fna3d
DISTVERSION=     20.10
CATEGORIES=      graphics
LICENSE=         ZLIB

USE_GITHUB=      yes
GH_ACCOUNT=      FNA-XNA
GH_PROJECT=      FNA3D
GH_TUPLE=        FNA-XNA:MojoShader:07ce8799af:MojoShader/MojoShader

USES=            cmake sdl
USE_SDL=         sdl2

CFLAGS+=         -I${LOCALBASE}/include

do-install:
	${CP} ${BUILD_WRKSRC}/libFNA3D.so.0.${DISTVERSION} ${STAGEDIR}${PREFIX}/lib/

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/lib/libFNA3D.so.0.${DISTVERSION}

PLIST_FILES=     lib/libFNA3D.so.0.${DISTVERSION}

.include <bsd.port.mk>
