# $NetBSD: Makefile,v 1.5 2019/05/06 09:17:13 sjmulder Exp $

DISTNAME=	nnn-2.4
CATEGORIES=	sysutils
MASTER_SITES=	${MASTER_SITE_GITHUB:=jarun/}
GITHUB_TAG=	v${PKGVERSION_NOREV}

MAINTAINER=	sjmulder@NetBSD.org
HOMEPAGE=	https://github.com/jarun/nnn/
COMMENT=	Optimized, feature-packed terminal file manager
LICENSE=	2-clause-bsd

USE_TOOLS+=	gmake pkg-config
USE_CURSES=	wide

# build without readline unless option set (see options.mk)
BUILD_TARGET=	norl

MAKE_ENV+=	MANPREFIX=${PREFIX}/${PKGMANDIR}
MAKE_ENV+=	CFLAGS_OPTIMIZATION=
MAKE_ENV+=	CFLAGS_CURSES=${BUILDLINK_CFLAGS.curses:Q}
MAKE_ENV+=	LDLIBS_CURSES=${BUILDLINK_LDADD.curses:Q}

.include "options.mk"

.include "../../mk/curses.buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
