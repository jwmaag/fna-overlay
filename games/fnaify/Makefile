PORTNAME=            fnaify
DISTVERSION=         3.0 
CATEGORIES=          games
LICENSE=             ISCL

USE_GITHUB=          yes
GH_ACCOUNT=          rfht
GH_PROJECT=          fnaify

USES=				 mono

RUN_DEPENDS=         oksh:shells/oksh \
                     ${LOCALBASE}/share/FNA/FNA.dll:games/fna \
					 ${LOCALBASE}/lib/steamworks-nosteam/Steamworks.NET.dll:games/steamworks-nosteam

LIB_DEPENDS=         libFAudio.so:audio/faudio \
                     libogg.so:audio/libogg \
                     libvorbis.so:audio/libvorbis \
					 libFNA3D.so:graphics/fna3d \
					 libmojoshader.so:graphics/mojoshader \
					 libtheora.so:multimedia/libtheora \
					 libtheorafile.so:multimedia/libtheorafile \
					 libstubborn.so:misc/libstubborn

MAKE_ARGS=           "DESTDIR=${STAGEDIR}"

NO_BUILD=            yes

.include <bsd.port.mk>
