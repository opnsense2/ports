PORTNAME=	google-iam-v1
PORTVERSION=	0.5.0
CATEGORIES=	devel rubygems
MASTER_SITES=	RG

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	Ruby Client for the IAM Policy API
WWW=		https://github.com/googleapis/google-cloud-ruby/tree/main/google-iam-v1

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE.md

RUN_DEPENDS=	rubygem-gapic-common>=0.19.0<2.0:devel/rubygem-gapic-common \
		rubygem-google-cloud-errors>=1.0<2:net/rubygem-google-cloud-errors \
		rubygem-grpc-google-iam-v1>=1.1<2:devel/rubygem-grpc-google-iam-v1

USES=		gem

NO_ARCH=	yes

.include <bsd.port.mk>
