# $NetBSD: Makefile,v 1.5 2019/02/03 16:10:44 taca Exp $

DISTNAME=	chef-config-14.10.9
CATEGORIES=	sysutils

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/chef/chef
COMMENT=	Chef's default configuration and config loading
LICENSE=	apache-2.0

DEPENDS+=	${RUBY_PKGPREFIX}-mixlib-config>=2.0<3:../../devel/ruby-mixlib-config
DEPENDS+=	${RUBY_PKGPREFIX}-mixlib-shellout>=2.0<3:../../devel/ruby-mixlib-shellout
DEPENDS+=	${RUBY_PKGPREFIX}-fuzzyurl>=0:../../textproc/ruby-fuzzyurl
DEPENDS+=	${RUBY_PKGPREFIX}-addressable>=0:../../net/ruby-addressable
DEPENDS+=	${RUBY_PKGPREFIX}-tomlrb>=1.2<2:../../devel/ruby-tomlrb

USE_LANGUAGES=	# none

.include "../../lang/ruby/gem.mk"
.include "../../mk/bsd.pkg.mk"
