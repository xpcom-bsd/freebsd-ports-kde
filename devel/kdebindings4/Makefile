# $FreeBSD$

PORTNAME=	kdebindings
PORTVERSION=	${KDE4_VERSION}
PORTREVISION=	1
CATEGORIES=	devel kde

MAINTAINER=	kde@FreeBSD.org
COMMENT=	KDE bindings (meta port)

USES=		kde:4 metaport

OPTIONS_DEFINE=	PERL PYTHON RUBY
OPTIONS_DEFAULT=	${OPTIONS_DEFINE}

PERL_DESC=	Perl bindings
PERL_USE=	KDE=perlkde_run

PYTHON_DESC=	Python bindings
PYTHON_RUN_DEPENDS=	${KDE_PREFIX}/lib/kde4/krosspython.so:devel/py-krosspython
PYTHON_USE=	KDE=pykde4_run,pykdeuic4_run

RUBY_DESC=	Ruby bindings
RUBY_RUN_DEPENDS=	${KDE_PREFIX}/lib/kde4/krossruby.so:devel/ruby-krossruby
RUBY_USE=	KDE=korundum_run

.include <bsd.port.mk>
