PORTNAME=	qcengine
DISTVERSION=	0.26.0
PORTREVISION=	1
CATEGORIES=	science python # chemistry
MASTER_SITES=	PYPI
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Quantum chemistry program executor and IO standardizer (QCSchema)
WWW=		https://github.com/MolSSI/QCEngine

LICENSE=	BSD3CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}py-cpuinfo>0:sysutils/py-py-cpuinfo@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}psutil>0:sysutils/py-psutil@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}pydantic>=1.8.2:devel/py-pydantic@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}qcelemental>=0.24.0:science/py-qcelemental@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}yaml>0:devel/py-yaml@${PY_FLAVOR}
TEST_DEPENDS=	${PYTHON_PKGNAMEPREFIX}pytest>0:devel/py-pytest@${PY_FLAVOR} \
		dftd4:science/dftd4 \
		mopac:science/mopac \
		mp2d:science/mp2d \
		mrchem:science/py-mrchem@${PY_FLAVOR} \
		nwchem:science/nwchem \
		rdkit>0:science/rdkit \
		s-dftd3:science/simple-dftd3 \
		xtb:science/xtb \
		${PYTHON_PKGNAMEPREFIX}msgpack>0:devel/py-msgpack@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}pyberny>0:science/py-pyberny@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}geometric>0:science/py-geometric@${PY_FLAVOR}
		# last dependencies above are for specific quantum chemistry packages to test with TODO torchani,openmm,psi4,torsiondrive,mdi

USES=		python
USE_PYTHON=	distutils concurrent autoplist pytest # 1 test fails, see https://github.com/MolSSI/QCEngine/issues/377, psi4 test hangs, see https://github.com/MolSSI/QCEngine/issues/390

NO_ARCH=	yes

.include <bsd.port.mk>
