# $NetBSD: Makefile,v 1.18 2019/04/25 07:33:29 maya Exp $

DISTNAME=	arandr-0.1.10
PKGREVISION=	1
CATEGORIES=	x11
MASTER_SITES=	http://christian.amsuess.com/tools/arandr/files/

MAINTAINER=	rga@sdf.lonestar.org
HOMEPAGE=	http://christian.amsuess.com/tools/arandr/
COMMENT=	Designed to provide a simple visual front end for XRandR
LICENSE=	gnu-gpl-v3

BUILD_DEPENDS+=	${PYPKGPREFIX}-docutils>=0.6:../../textproc/py-docutils
DEPENDS+=	${PYPKGPREFIX}-gobject3-[0-9]*:../../devel/py-gobject3

.include "../../mk/bsd.prefs.mk"

.if ${X11_TYPE} != "native"
DEPENDS+=	xrandr>=1.2:../../x11/xrandr
.endif

PY_PATCHPLIST=			YES
PYSETUP=			setup.py
PYTHON_VERSIONS_INCOMPATIBLE=	27

# Adjust setup.py
SUBST_CLASSES+=		setup
SUBST_STAGE.setup=	pre-configure
SUBST_MESSAGE.setup=	Fixing ${PYSETUP}
SUBST_FILES.setup=	${PYSETUP}
SUBST_SED.setup+=	-e 's,share/man/,${PKGMANDIR}/,g'

.include "../../lang/python/distutils.mk"
.include "../../sysutils/desktop-file-utils/desktopdb.mk"
.include "../../mk/bsd.pkg.mk"
