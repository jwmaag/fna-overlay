PORTNAME=             tshock-server
DISTVERSIONPREFIX=    v
DISTVERSION=          4.5.7

CATEGORIES=     games
MAINTAINER=     jwmaag@gmail.com
COMMENT=        Port of the Terraria server Tshock
LICENSE=        GPLv3

BUILD_DEPENDS=  msbuild:devel/msbuild
NUGET_DEPENDS=	BCrypt.Net=0.1.0 \
  MySql.Data=6.9.8 \
  Newtonsoft.Json=10.0.3 \
  ILRepack.Lib=2.0.15 \
  Microsoft.Web.Xdt=2.1.1 \
  Mono.Cecil=0.9.6.4 \
  NDesk.Options=0.2.1 \
  NuGet.Core=2.14.0 \
  OTAPI=2.0.0.46 \
  OTAPI.Patcher=2.0.0.41

USES=           mono:nuget

USE_GITHUB=     yes
GH_ACCOUNT=     pryaxis
GH_PROJECT=     TShock

GH_TUPLE=       Pryaxis:TSAPI:b9a0fdf:TSAPI/TerrariaServerAPI


post-extract:
	${CP} ${FILESDIR}/Makefile ${WRKSRC}/Makefile

do-install:
	${MKDIR} ${STAGEDIR}/${PREFIX}/libexec/tshock
	${CP} -r ${WRKSRC}/Output/* ${STAGEDIR}/${PREFIX}/libexec/tshock/
	${CP} ${FILESDIR}/tshock ${STAGEDIR}/${PREFIX}/bin/

.include <bsd.port.mk>
