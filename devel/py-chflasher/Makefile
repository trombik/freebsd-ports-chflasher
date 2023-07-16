PORTNAME=	chflasher
DISTVERSION=	2022.06.27
CATEGORIES=	devel python
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	y@trombik.org
COMMENT=	Python based flash/verify tool for the CH55x MCUs
WWW=	https://github.com/hexeguitar/CH55x_python_flasher

LICENSE=	GPLv3
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}pyserial>=3.0:comms/py-pyserial@${PY_FLAVOR} \
	${PYTHON_PKGNAMEPREFIX}pyusb>=0:devel/py-pyusb@${PY_FLAVOR}

USES=		python

USE_GITHUB=	yes
GH_TUPLE=	hexeguitar:CH55x_python_flasher:73fc5c5
PLIST_FILES=	chflasher
NO_BUILD=	yes

do-install:
	${INSTALL_SCRIPT} ${WRKSRC}/chflasher.py ${STAGEDIR}${PREFIX}/bin/${PORTNAME}

.include <bsd.port.mk>
