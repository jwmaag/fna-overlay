PORTNAME=        fna
DISTVERSION=     21.05
MAINTAINER=      jwmaag@gmail.com
CATEGORIES=      games

LICENSE=         MSPL
LICENSE_NAME=    Microsoft Public License (Ms-PL)
LICENSE_FILE=	 ${WRKSRC}/licenses/LICENSE
LICENSE_PERMS=   dist-mirror pkg-mirror auto-accept

USE_GITHUB=      yes
GH_ACCOUNT=      FNA-XNA
GH_PROJECT=      FNA

GH_TUPLE=        FNA-XNA:FAudio:03b92fc:FAudio/lib/FAudio \
                 FNA-XNA:FNA3D:6e2676f:FNA3D/lib/FNA3D \
                 FNA-XNA:Theorafile:3f8bd6c:Theorafile/lib/Theorafile \
                 flibitijibibo:SDL2-CS:fadd013:SDL2_CS/lib/SDL2-CS 

USES=            mono sdl
USE_SDL=         sdl2 image2 mixer2 ttf2
LIB_DEPENDS=     libtheorafile.so:multimedia/libtheorafile \
                 libFNA3D.so:graphics/fna3d \
                 libFAudio.so:audio/faudio 
				 

# CFLAGS+=         -I${LOCALBASE}/include

do-install:
	${MKDIR} -p ${STAGEDIR}${PREFIX}/share/FNA/
	${CP} ${BUILD_WRKSRC}/bin/Release/FNA.dll ${STAGEDIR}${PREFIX}/share/FNA/
	${CP} ${BUILD_WRKSRC}/bin/Release/FNA.dll.config ${STAGEDIR}${PREFIX}/share/FNA/

PLIST_FILES=     share/FNA/FNA.dll \
				 share/FNA/FNA.dll.config

.include <bsd.port.mk>
