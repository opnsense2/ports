PORTNAME=	Compiler-Lexer
PORTVERSION=	0.23
CATEGORIES=	devel perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	perl@FreeBSD.org
COMMENT=	Perl extension for lexical analyzer
WWW=		https://metacpan.org/release/Compiler-Lexer

LICENSE=	ART10 GPLv1+
LICENSE_COMB=	dual

BUILD_DEPENDS=	p5-Module-Build-XSUtil>0:devel/p5-Module-Build-XSUtil

USES=		perl5
USE_PERL5=	modbuild

.include <bsd.port.options.mk>

.if ${OPSYS} == FreeBSD && ${OSVERSION} >= 1400091
CFLAGS+=  -Dregister=
.endif

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/${SITE_ARCH_REL}/auto/Compiler/Lexer/Lexer.so

.include <bsd.port.mk>
