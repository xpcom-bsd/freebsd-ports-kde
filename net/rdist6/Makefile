# Created by: peter
# $FreeBSD$

PORTNAME=	rdist
PORTVERSION=	6.1.5
PORTREVISION=	5
CATEGORIES=	net
MASTER_SITES=	http://www.magnicomp.com/download/rdist/ \
		ftp://ftp.sunet.se/pub/unix/admin/mirror-magnicomp/download/rdist/

MAINTAINER=	cy@FreeBSD.org
COMMENT=	Network file distribution/synchronisation utility

# To avoid confusion with /usr/bin/rdist, you may prefer otherwise.
RDIST_NAME?=	rdist6

INSTALL_TARGET=	install install.man
MAKE_ENV=	BUILD_OPT="${CFLAGS}" BUILD_CLIENT=${RDIST_NAME} \
		STAGEDIR=${STAGEDIR}
PLIST_SUB=	RDIST_NAME=${RDIST_NAME}

.include <bsd.port.pre.mk>

.if ${OPSYS} == FreeBSD && ${OSVERSION} <= 1200050
RUN_DEPENDS=	rsh:net/bsdrcmds
.endif

post-install:
	@${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/${RDIST_NAME}
	@${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/rdistd

.include <bsd.port.post.mk>
