# $NetBSD: Makefile,v 1.7 2019/04/16 18:41:17 bsiegert Exp $

DISTNAME=	sync-0.0.20180314
PKGNAME=	go-${DISTNAME}
PKGREVISION=	6
CATEGORIES=	devel
MASTER_SITES=	${MASTER_SITE_GITHUB:=golang/}
GITHUB_PROJECT=	${PKGBASE:S/go-//}
GITHUB_TAG=	1d60e4601c6fd243af51cc01ddf169918a5407ca

MAINTAINER=	minskim@NetBSD.org
HOMEPAGE=	http://golang.org/
COMMENT=	Concurrency primitives for Go
LICENSE=	modified-bsd

GO_SRCPATH=	golang.org/x/sync
GO_DIST_BASE=	${PKGBASE:S/go-//}-${GITHUB_TAG}

.include "../../net/go-net/buildlink3.mk"
.include "../../lang/go/go-package.mk"
.include "../../mk/bsd.pkg.mk"
