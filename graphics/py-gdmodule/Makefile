# $NetBSD: Makefile,v 1.16 2019/04/26 14:12:40 maya Exp $

DISTNAME=	gdmodule-0.59
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
PKGREVISION=	2
CATEGORIES=	graphics python
MASTER_SITES=	${MASTER_SITE_GITHUB:=Solomoriah/}
GITHUB_PROJECT=	gdmodule
GITHUB_TAG=	v0.59

MAINTAINER=	darcy@NetBSD.org
HOMEPAGE=	https://github.com/Solomoriah/gdmodule
COMMENT=	Python interface to gd graphics library
LICENSE=	original-bsd

PYTHON_VERSIONS_INCOMPATIBLE=	36 37 # not yet ported as of 0.59

SUBST_CLASSES+=		pkgpath
SUBST_STAGE.pkgpath=	pre-configure
SUBST_MESSAGE.pkgpath=	Use correct pkgsrc prefix.
SUBST_FILES.pkgpath=	setup.py
SUBST_SED.pkgpath=	-e 's,"/usr/local,"${PREFIX},g'
SUBST_SED.pkgpath+=	-e 's,"png","png16",g'

BUILDLINK_API_DEPENDS.gd+=	gd>=2.0.23
.include "../../graphics/gd/buildlink3.mk"
.include "../../graphics/giflib/buildlink3.mk"
.include "../../x11/Xaw-Xpm/buildlink3.mk"
.include "../../lang/python/distutils.mk"
.include "../../mk/bsd.pkg.mk"
