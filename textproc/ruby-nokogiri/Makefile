# $NetBSD: Makefile,v 1.45 2019/03/10 11:24:17 tsutsui Exp $

DISTNAME=	nokogiri-1.10.1
CATEGORIES=	textproc

MAINTAINER=	tsutsui@NetBSD.org
HOMEPAGE=	http://nokogiri.org/
COMMENT=	HTML, XML, SAX, and Reader parser with XPath and CSS selector support
LICENSE=	mit

RUBY_VERSIONS_INCOMPATIBLE= 22

DEPENDS+=	${RUBY_PKGPREFIX}-mini_portile2>=2.4.0<2.5.0:../../misc/ruby-mini_portile2

USE_GCC_RUNTIME=	yes
USE_TOOLS+=		pkg-config
MAKE_ENV+=		NOKOGIRI_USE_SYSTEM_LIBRARIES=yes
RUBYGEM_OPTIONS+=	--format-executable
OVERRIDE_GEMSPEC+=	:files ports/archives/libxml2-2.9.9.tar.gz= \
				ports/archives/libxslt-1.1.33.tar.gz=

.include "../../devel/ruby-pkg-config/tool.mk"
.include "../../textproc/libxml2/buildlink3.mk"
.include "../../textproc/libxslt/buildlink3.mk"
.include "../../lang/ruby/gem.mk"
.include "../../mk/bsd.pkg.mk"
