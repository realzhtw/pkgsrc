# $NetBSD: Makefile,v 1.50 2019/05/05 22:49:46 ryoon Exp $

PKGNAME=	pidgin-sametime-${PIDGIN_VERSION}
PKGREVISION=	2

COMMENT=	Lotus Sametime plugin for the Pidgin instant messenger

.include "../../chat/libpurple/Makefile.common"

USE_TOOLS+=		msgfmt perl intltool

CONFIGURE_ARGS+=	--enable-meanwhile

BUILD_DIRS=		libpurple/protocols/sametime

.include "../../chat/libpurple/buildlink3.mk"
.include "../../chat/meanwhile/buildlink3.mk"
.include "../../converters/libiconv/buildlink3.mk"
.include "../../devel/GConf/schemas.mk"
.include "../../devel/glib2/buildlink3.mk"
.include "../../devel/libidn/buildlink3.mk"
.include "../../textproc/libxml2/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
