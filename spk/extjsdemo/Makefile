SPK_NAME = extjsdemo
SPK_VERS = 1.0
SPK_REV = 1
SPK_ICON = src/extjsdemoapp.png
WIZARDS_DIR = WIZARD_UIFILES
DSM_UI_DIR = app

DEPENDS = 

MAINTAINER = DigitalBox98

DESCRIPTION = ExtJS Demo application to illustrate the usage of Syno ExtJS framework for DSM applications.
DISPLAY_NAME = ExtJSDemo

STARTABLE=no

HOMEPAGE = https://github.com/DigitalBox98/spksrc

CONF_DIR = src/conf
SYSTEM_GROUP = http

# Make sure ARCH is not defined
override ARCH=

COPY_TARGET = nop

POST_STRIP_TARGET = extjsdemo_extra_install

include ../../mk/spksrc.spk.mk

.PHONY: extjsdemo_extra_install
extjsdemo_extra_install:
	install -m 755 -d $(STAGING_DIR)/app/
	install -m 644 src/app/config $(STAGING_DIR)/app/config
	install -m 644 src/app/extjsdemo.js $(STAGING_DIR)/app/extjsdemo.js
	install -m 644 src/app/helptoc.conf $(STAGING_DIR)/app/helptoc.conf
	install -m 755 -d $(STAGING_DIR)/app/help
	for language in enu fre; do \
		install -m 755 -d $(STAGING_DIR)/app/help/$${language}; \
		install -m 644 src/app/help/$${language}/extjsdemo_index.html $(STAGING_DIR)/app/help/$${language}/extjsdemo_index.html; \
	done
	install -m 755 -d $(STAGING_DIR)/app/texts
	for language in enu fre; do \
		install -m 755 -d $(STAGING_DIR)/app/texts/$${language}; \
		install -m 644 src/app/texts/$${language}/strings $(STAGING_DIR)/app/texts/$${language}/strings; \
	done
	install -m 755 -d $(STAGING_DIR)/app/images
	install -m 644 src/app/images/* $(STAGING_DIR)/app/images/
