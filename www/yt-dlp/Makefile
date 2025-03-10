PORTNAME=	yt-dlp
DISTVERSION=	2023.06.22
CATEGORIES=	www
MASTER_SITES=	https://github.com/${PORTNAME}/${PORTNAME}/releases/download/${DISTVERSION}/
DISTNAME=	${PORTNAME}
DIST_SUBDIR=	${PORTNAME}/${DISTVERSION}

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Command-line program for downloading videos from various platforms
WWW=		https://github.com/yt-dlp/yt-dlp

LICENSE=	UNLICENSE
LICENSE_FILE=	${WRKSRC}/LICENSE

PY_DEPENDS=	${PYTHON_PKGNAMEPREFIX}brotli>0:archivers/py-brotli@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}certifi>0:security/py-certifi@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}mutagen>0:audio/py-mutagen@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}pycryptodomex>0:security/py-pycryptodomex@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}sqlite3>0:databases/py-sqlite3@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}websockets>0:devel/py-websockets@${PY_FLAVOR}
BUILD_DEPENDS=	${PY_DEPENDS}
RUN_DEPENDS=	${PY_DEPENDS}

USES=		gmake python shebangfix

SHEBANG_GLOB=	devscripts/*.py

MAKE_ARGS=	PYTHON=${PYTHON_CMD}

NO_ARCH=	yes

OPTIONS_DEFINE=		FFMPEG RTMPDUMP SYMLINK
OPTIONS_DEFAULT=	FFMPEG RTMPDUMP SYMLINK
OPTIONS_SUB=		yes

FFMPEG_RUN_DEPENDS=	ffprobe:multimedia/ffmpeg

RTMPDUMP_DESC=		Use rtmpdump to download rtmp video streams
RTMPDUMP_RUN_DEPENDS=	rtmpdump:multimedia/rtmpdump

SYMLINK_DESC=		Install youtube-dl symbolic link for executable
SYMLINK_CONFLICTS=	youtube_dl

post-install-SYMLINK-on:
	@${RLN} ${STAGEDIR}${PREFIX}/bin/yt-dlp ${STAGEDIR}${PREFIX}/bin/youtube-dl

.include <bsd.port.mk>
