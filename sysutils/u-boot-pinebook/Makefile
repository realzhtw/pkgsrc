# $NetBSD: Makefile,v 1.13 2019/05/07 14:06:25 thorpej Exp $

UBOOT_VERSION=		2018.11rc3
UBOOT_TARGET=		pinebook
UBOOT_CONFIG=		pinebook_defconfig
UBOOT_BIN=		u-boot-sunxi-with-spl.bin

UBOOT_INSTALLBOOT_PLIST=installboot.plist

# Use anarsoul's fork of mainline U-Boot with Pinebook support patched in
MASTER_SITES=		${MASTER_SITE_GITHUB:=anarsoul/}
GITHUB_PROJECT=		u-boot-pine64
GITHUB_TAG=		88eea875b3b82a0e50cbb112e0aea2259dc2e011
DISTNAME=		u-boot-${UBOOT_TARGET}-${UBOOT_VERSION}
EXTRACT_SUFX=		.tar.gz
PKGREVISION=		3

DISTINFO_FILE=		${.CURDIR}/../../sysutils/u-boot-pinebook/distinfo
PATCHDIR=		${.CURDIR}/../../sysutils/u-boot-pinebook/patches

post-extract:
	${CP} ${PREFIX}/share/arm-trusted-firmware/sun50i_a64/bl31.bin ${WRKSRC}

post-build:
	${CAT} ${WRKSRC}/spl/sunxi-spl.bin ${WRKSRC}/u-boot.itb > ${WRKSRC}/u-boot-sunxi-with-spl.bin

.include "../../sysutils/arm-trusted-firmware-sun50i_a64/buildlink3.mk"
.include "../../sysutils/u-boot/u-boot-arm64.mk"

CHECK_PORTABILITY_SKIP+=tools/imx_cntr_image.sh
