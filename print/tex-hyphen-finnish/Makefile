# $NetBSD: Makefile,v 1.9 2019/05/11 06:57:25 markd Exp $

DISTNAME=	hyphen-finnish
PKGNAME=	tex-${DISTNAME}-2019
TEXLIVE_REV=	50792

MAINTAINER=	minskim@NetBSD.org
COMMENT=	Hyphenation patterns for Finnish language
LICENSE=	lppl-1.3c

DEPENDS+=	tex-hyphen-base-[0-9]*:../../print/tex-hyphen-base
DEPENDS+=	tex-hyph-utf8-[0-9]*:../../print/tex-hyph-utf8

TEX_HYPHEN_DAT+=	finnish loadhyph-fi.tex
TEX_HYPHEN_DEF+=	\\addlanguage{finnish}{loadhyph-fi.tex}{}{2}{2}
TEX_HYPHEN_LUA+=	['finnish']={ \
			  loader='loadhyph-fi.tex', \
			  lefthyphenmin=2, \
			  righthyphenmin=2, \
			  synonyms={}, \
			  patterns='hyph-fi.pat.txt', \
			  hyphenation='', \
			},

.include "../../print/texlive/package.mk"
.include "../../mk/bsd.pkg.mk"
