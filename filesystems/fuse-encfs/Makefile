# $NetBSD: Makefile,v 1.17 2019/04/10 12:33:01 gdt Exp $
#

GITHUB_PROJECT=	encfs
GITHUB_TAG=	v${PKGVERSION_NOREV}
DISTNAME=	encfs-1.9.4
PKGNAME=	fuse-${DISTNAME}
PKGREVISION=	2
CATEGORIES=	filesystems
MASTER_SITES=	${MASTER_SITE_GITHUB:=vgough/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://www.arg0.net/encfs
COMMENT=	FUSE Encrypted Filesystem
LICENSE=	gnu-gpl-v3


USE_TOOLS+=	autoconf cmake pkg-config
USE_CMAKE=	yes
USE_LANGUAGES=	c c++

CONFIGURE_DIRS=	${WRKDIR}/build
CMAKE_ARG_PATH=	${WRKSRC}

# Remediate open-coding in cmake that badly reimplements autoconf's
# --mandir=.
# \todo File a bug upstream.
SUBST_CLASSES+=		mandir
SUBST_STAGE.mandir=	pre-configure
SUBST_MESSAGE.mandir=	Remediating cmake PKGMANDIR
SUBST_FILES.mandir=	CMakeLists.txt
SUBST_SED.mandir=	-E -e "/MAN_DESTINATION/s,share/man,${PKGMANDIR},"

# \todo Add TEST_DEPENDS for unittest, after finding it or packaging
# it.
TEST_TARGET=	test

post-extract:
	${RUN} mkdir -p ${WRKDIR}/build

.include "../../security/openssl/buildlink3.mk"
.include "../../mk/fuse.buildlink3.mk"
.include "../../mk/pthread.buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
