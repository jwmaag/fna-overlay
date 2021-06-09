PORTNAME=	xoreos
DISTVERSIONPREFIX= v
DISTVERSION= 0.0.6
CATEGORIES=	games

MAINTAINER=	jwmaag@gmail.com
COMMENT=	Open source implemtnation of Bioware's Aurora engine
LICENSE=    GPLv3
USES=	    cmake compiler:c++11-lang gl openal sdl

USE_GITHUB= yes
GH_ACCOUNT= xoreos
GH_PROJECT= xoreos

USE_SDL=	sdl2
USE_GL=     gl glew glu

LIB_DEPENDS= libboost_system.so:devel/boost-libs \
	libfaad.so:audio/faad \
	libxml2.so:textproc/libxml2 \
	libfreetype.so:print/freetype2 \
	libogg.so:audio/libogg \
	libmad.so:audio/libmad \
	libvorbis.so:audio/libvorbis \
	libvpx.so:multimedia/libvpx \
	libxvidcore.so:multimedia/xvid

MAKE_JOBS_UNSAFE=   yes

PLIST_FILES=	bin/xoreos

do-install: 
	${INSTALL_PROGRAM} ${BUILD_WRKSRC}/bin/xoreos ${STAGEDIR}${PREFIX}/bin 

.include <bsd.port.mk>
