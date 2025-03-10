PORTNAME=	tox
PORTVERSION=	3.28.0
PORTREVISION=	1
CATEGORIES=	devel python
MASTER_SITES=	PYPI
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	bofh@FreeBSD.org
COMMENT=	Virtualenv-based automation of test activities
WWW=		https://tox.readthedocs.org/

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

BUILD_DEPENDS=	${PYTHON_PKGNAMEPREFIX}setuptools_scm>0:devel/py-setuptools_scm@${PY_FLAVOR}
RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}filelock>=3.0.0<4:sysutils/py-filelock@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}packaging>=14:devel/py-packaging@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}pluggy>=0.12.0:devel/py-pluggy@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}py>=1.4.17<2:devel/py-py@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}six>=1.14.0<2:devel/py-six@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}toml>=0.9.4:textproc/py-toml@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}tomli>0:textproc/py-tomli@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}virtualenv>=16.0.0:devel/py-virtualenv@${PY_FLAVOR}
TEST_DEPENDS=	${PYTHON_PKGNAMEPREFIX}flaky>=3.4.0:devel/py-flaky@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}freezegun>=0.3.11:devel/py-freezegun@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}pytest-mock>=1.10.0:devel/py-pytest-mock@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}pytest-xdist>=1.22.2:devel/py-pytest-xdist@${PY_FLAVOR}

USES=		python
USE_PYTHON=	autoplist concurrent distutils pytest4

NO_ARCH=	yes

# tox.ini clobbers our pytest arguments
post-extract:
	${RM} ${WRKSRC}/tox.ini

.include <bsd.port.mk>
