# $NetBSD: Makefile,v 1.6 2019/04/07 13:04:10 wen Exp $

CATEGORIES=	devel

MAINTAINER=	minskim@NetBSD.org
HOMEPAGE=	${R_HOMEPAGE_BASE}/repr/
COMMENT=	Serializable representations
LICENSE=	gnu-gpl-v3

DEPENDS+=	R-htmltools-[0-9]*:../../textproc/R-htmltools
DEPENDS+=	R-base64enc-[0-9]*:../../converters/R-base64enc
DEPENDS+=	R-jsonlite>=0:../../textproc/R-jsonlite

R_PKGNAME=	repr
R_PKGVER=	0.19.2

USE_LANGUAGES=	# none

BUILDLINK_API_DEPENDS.R+=	R>=3.0.1
.include "../../math/R/Makefile.extension"
.include "../../mk/bsd.pkg.mk"
