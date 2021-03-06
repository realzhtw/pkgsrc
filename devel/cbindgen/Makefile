# $NetBSD: Makefile,v 1.6 2019/05/15 12:24:01 ryoon Exp $

DISTNAME=	cbindgen-0.8.7
CATEGORIES=	devel
MASTER_SITES=	${MASTER_SITE_GITHUB:=eqrion/}
GITHUB_PROJECT=	cbindgen
GITHUB_TAG=	v${PKGVERSION_NOREV}

MAINTAINER=	ryoon@NetBSD.org
HOMEPAGE=	https://github.com/eqrion/cbindgen/releases
COMMENT=	Generating C bindings from Rust code
LICENSE=	mpl-2.0

CARGO_CRATE_DEPENDS+=	\
	ansi_term-0.11.0 \
	atty-0.2.11 \
	autocfg-0.1.2 \
	bitflags-1.0.4 \
	cfg-if-0.1.6 \
	clap-2.32.0 \
	cloudabi-0.0.3 \
	fuchsia-zircon-0.3.3 \
	fuchsia-zircon-sys-0.3.3 \
	itoa-0.4.3 \
	libc-0.2.47 \
	log-0.4.6 \
	proc-macro2-0.4.25 \
	quote-0.6.10 \
	rand-0.6.4 \
	rand_chacha-0.1.1 \
	rand_core-0.3.0 \
	rand_hc-0.1.0 \
	rand_isaac-0.1.1 \
	rand_os-0.1.1 \
	rand_pcg-0.1.1 \
	rand_xorshift-0.1.1 \
	rdrand-0.4.0 \
	redox_syscall-0.1.50 \
	redox_termios-0.1.1 \
	remove_dir_all-0.5.1 \
	rustc_version-0.2.3 \
	ryu-0.2.7 \
	semver-0.9.0 \
	semver-parser-0.7.0 \
	serde-1.0.84 \
	serde_derive-1.0.84 \
	serde_json-1.0.36 \
	strsim-0.7.0 \
	syn-0.15.26 \
	tempfile-3.0.5 \
	termion-1.5.1 \
	textwrap-0.10.0 \
	toml-0.4.10 \
	unicode-width-0.1.5 \
	unicode-xid-0.1.0 \
	vec_map-0.8.1 \
	winapi-0.3.6 \
	winapi-i686-pc-windows-gnu-0.4.0 \
	winapi-x86_64-pc-windows-gnu-0.4.0

INSTALLATION_DIRS=	bin

do-build:
	cd ${WRKSRC} && ${SETENV} ${MAKE_ENV} ${PREFIX}/bin/cargo build --locked --frozen --release

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/target/release/cbindgen ${DESTDIR}${PREFIX}/bin

.include "../../lang/rust/cargo.mk"
.include "../../lang/rust/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
