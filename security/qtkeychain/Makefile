# $OpenBSD: Makefile.template,v 1.71 2014/07/10 12:33:17 sthen Exp $

COMMENT =		Qt API to store passwords and other secret data

DISTNAME =		qtkeychain-${GH_TAGNAME:S/v//}

SHARED_LIBS =		qtkeychain	0.0 # 0.4

CATEGORIES =		security

MAINTAINER =		Kirill Bychkov <kirby@openbsd.org>

# BSD-like
PERMIT_PACKAGE_CDROM =	Yes

WANTLIB =		QtDBus m stdc++

GH_ACCOUNT =		frankosterfeld
GH_PROJECT =		qtkeychain
GH_TAGNAME =		v0.4.0

MODULES =		devel/cmake x11/qt4

NO_TEST =		Yes

.include <bsd.port.mk>
