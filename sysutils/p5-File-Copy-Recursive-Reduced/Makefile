# $NetBSD: Makefile,v 1.2 2018/08/22 09:46:36 wiz Exp $

DISTNAME=	File-Copy-Recursive-Reduced-0.006
PKGNAME=	p5-${DISTNAME}
PKGREVISION=	1
CATEGORIES=	sysutils devel perl5
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=../by-module/File/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://search.cpan.org/dist/File-Copy-Recursive/
COMMENT=	Recursive copying of files and directories
LICENSE=	${PERL5_LICENSE}

BUILD_DEPENDS+=	p5-Capture-Tiny>=0:../../devel/p5-Capture-Tiny
BUILD_DEPENDS+=	p5-Path-Tiny>=0:../../filesystems/p5-Path-Tiny

USE_LANGUAGES=	# empty
PERL5_PACKLIST=	auto/File/Copy/Recursive/Reduced/.packlist

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
