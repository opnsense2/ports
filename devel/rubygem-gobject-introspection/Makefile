PORTNAME=	gobject-introspection
PORTVERSION=	4.1.7
CATEGORIES=	devel rubygems
MASTER_SITES=	RG

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	Ruby binding of GObject Introspection
WWW=		https://ruby-gnome.github.io/ \
		https://github.com/ruby-gnome/ruby-gnome

LICENSE=	LGPL21+
LICENSE_FILE=	${WRKSRC}/COPYING.LIB

BROKEN_sparc64=	does not build: fails to compile rb-gi-function-info.c

RUN_DEPENDS=	rubygem-glib2>=${PORTVERSION}<${PORTVERSION}_99:devel/rubygem-glib2

USES=		gem gnome
USE_GNOME=	introspection

.include <bsd.port.mk>
