PORTNAME=        fna
DISTVERSION=     21.05
MAINTAINER=      jwmaag@gmail.com
CATEGORIES=      games

LICENSE=         MSPL
LICENSE_NAME=    Microsoft Public License (Ms-PL)
LICENSE_FILE=	 ${WRKSRC}/licences/LICENSE
LICENSE_PERMS=   dist-mirror pkg-mirror dist-sell pkg-sell auto-accept

USE_GITHUB=      yes
GH_ACCOUNT=      FNA-XNA
GH_PROJECT=      FNA

USES=            mono

# depends faudio, sdlimage, fna3d, mojoshader, vorbisfile, ...
# LIB_DEPENDS=     
# RUN_DEPENDS=     

CFLAGS+=         -I${LOCALBASE}/include

.include <bsd.port.mk>
