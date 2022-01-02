PKG_NAME = aria2
PKG_VERS = 1.36.0
PKG_EXT = tar.xz
PKG_DIST_NAME = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = https://github.com/aria2/aria2/releases/download/release-$(PKG_VERS)
PKG_DIR = $(PKG_NAME)-$(PKG_VERS)

DEPENDS = cross/libssh2 cross/gnutls cross/libgcrypt cross/expat cross/c-ares cross/sqlite

# archs with too old c++ compiler (c++ 11 is required)
UNSUPPORTED_ARCHS = $(ARMv5_ARCHS) $(OLD_PPC_ARCHS)

HOMEPAGE = https://aria2.github.io/
COMMENT  = aria2 is a lightweight multi-protocol & multi-source command-line download utility. It supports HTTP/HTTPS, FTP, SFTP, BitTorrent and Metalink.
LICENSE  = GPLv2

GNU_CONFIGURE = 1

CONFIGURE_ARGS  = --with-ca-bundle=/etc/ssl/certs/ca-certificates.crt
CONFIGURE_ARGS += --with-sqlite3

include ../../mk/spksrc.cross-cc.mk