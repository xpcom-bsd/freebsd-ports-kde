# $FreeBSD$

PORTNAME=	xf86-input-synaptics
PORTVERSION=	1.9.0
CATEGORIES=	x11-drivers

MAINTAINER=	x11@FreeBSD.org
COMMENT=	X.Org synaptics input driver

LICESNE=	MIT
LICENSE_FILE=	${WRKSRC}/COPYING

USES=		pathfix
USE_XORG=	x11 xtst
XORG_CAT=	driver

OPTIONS_DEFINE=	EVDEV
EVDEV_DESC=	Use evdev for input events (requires kernel support)

EVDEV_CONFIGURE_ENV=	BUILD_EVENTCOMM=yes
EVDEV_BUILD_DEPENDS=	${LOCALBASE}/include/linux/input.h:multimedia/v4l_compat
EVDEV_LIB_DEPENDS=	libevdev.so:devel/libevdev

.include <bsd.port.mk>
