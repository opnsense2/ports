PORTNAME=	yar
PORTVERSION=	2.3.2
CATEGORIES=	www

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	Yar (Yet another RPC framework) is a light, concurrent RPC framework
WWW=		https://pecl.php.net/package/yar

LICENSE=	PHP301
LICENSE_FILE=	${WRKSRC}/LICENSE

LIB_DEPENDS=	libcurl.so:ftp/curl

USES=		localbase:ldflags php:build,pecl
USE_PHP=	curl

IGNORE_WITH_PHP=82 83

OPTIONS_DEFINE=	MSGPACK
OPTIONS_DEFAULT=MSGPACK
MSGPACK_DESC=	Enable MSGPACK module

MSGPACK_BUILD_DEPENDS=	${PECL_PKGNAMEPREFIX}msgpack>=0:devel/pecl-msgpack@${PHP_FLAVOR}
MSGPACK_RUN_DEPENDS=	${PECL_PKGNAMEPREFIX}msgpack>=0:devel/pecl-msgpack@${PHP_FLAVOR}

.include <bsd.port.mk>
