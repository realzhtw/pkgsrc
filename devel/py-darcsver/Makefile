# $NetBSD: Makefile,v 1.12 2019/04/26 14:12:35 maya Exp $

DISTNAME=	darcsver-1.7.4
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	devel
MASTER_SITES=	${MASTER_SITE_PYPI:=d/darcsver/}

MAINTAINER=	gdt@ir.bbn.com
HOMEPAGE=	https://pypi.python.org/pypi/darcsver/
COMMENT=	Generate a version number from darcs history
LICENSE=	modified-bsd

DEPENDS+=		${PYPKGPREFIX}-expat>=0:../../textproc/py-expat

USE_LANGUAGES=	# none

PYTHON_VERSIONS_INCOMPATIBLE=	36 37 # not yet ported as of 1.7.4

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
