PORTNAME=            libstubborn
DISTVERSION=         0.1
CATEGORIES=          misc

USE_GITHUB=          yes
GH_ACCOUNT=          rfht
GH_PROJECT=          libstubborn

# MAKE_ARGS=           "PREFIX=${STAGEDIR}/${PREFIX}"
#
do-install:
	${CP} ${BUILD_WRKSRC}/libstubborn.so.0.0 ${STAGEDIR}/${PREFIX}/lib/
	${RLN} ${STAGEDIR}/${PREFIX}/lib/libstubborn.so.0.0 ${STAGEDIR}/${PREFIX}/lib/libstubborn.so.0 
	${RLN} ${STAGEDIR}/${PREFIX}/lib/libstubborn.so.0.0 ${STAGEDIR}/${PREFIX}/lib/libstubborn.so

post-install:
	${STRIP_CMD} ${STAGEDIR}/${PREFIX}/lib/libstubborn.so.0.0 

PLIST_FILES=        lib/libstubborn.so.0.0 \
					lib/libstubborn.so.0 \
					lib/libstubborn.so

.include <bsd.port.mk>
