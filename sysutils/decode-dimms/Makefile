# $NetBSD: Makefile,v 1.14 2019/04/08 00:16:06 pgoyette Exp $

# no Release yet
_DATE=		20190405
PKGREVISION=	1
GIT_COMMIT=	cea0000657a2dde506df91ecce6b18ac2d7224db
DISTNAME=	i2c-tools-${GIT_COMMIT}
PKGNAME=	decode-dimms-0.0.${_DATE}
CATEGORIES=	sysutils
MASTER_SITES=	https://git.kernel.org/pub/scm/utils/i2c-tools/i2c-tools.git/snapshot/

MAINTAINER=	pgoyette@NetBSD.org
HOMEPAGE=	https://git.kernel.org/pub/scm/utils/i2c-tools/
COMMENT=	Decode memory DIMM SPD ROM info
LICENSE=	gnu-gpl-v2

USE_TOOLS+=	perl:run
REPLACE_PERL=	eeprom/decode-dimms

SUBST_CLASSES+=		rev
SUBST_STAGE.rev=	pre-patch
SUBST_FILES.rev=        eeprom/decode-dimms
SUBST_SED.rev=          -e 's/^$$revision = .*;/$$revision = "${_DATE}-${GIT_COMMIT}";/'
SUBST_SED.rev+=		-e '/^$$revision =~/d'

NO_BUILD=	yes

USE_LANGUAGES=	# empty

ONLY_FOR_PLATFORM= NetBSD-*-*

INSTALLATION_DIRS=	bin ${PKGMANDIR}/man1

do-install:
	${INSTALL_SCRIPT} ${WRKSRC}/eeprom/decode-dimms \
		${DESTDIR}${PREFIX}/bin/decode-dimms
	${INSTALL_MAN} ${WRKSRC}/eeprom/decode-dimms.1 \
		${DESTDIR}${PREFIX}/${PKGMANDIR}/man1/decode-dimms.1

.include "../../mk/bsd.pkg.mk"
