# $OpenBSD: Makefile,v 1.28 2015/05/22 11:31:17 ajacoutot Exp $

SHARED_LIBS =		rtmp 1.0

COMMENT =		dump RTMP media streams

RVER =			2.4pl7
DISTNAME =		rtmpdump-${RVER}
REVISION =		2
WRKDIST =		${WRKDIR}/rtmpdump

CATEGORIES =		net

HOMEPAGE =		http://rtmpdump.mplayerhq.hu/

# tools GPLv2+, librtmp LGPLv2.1+
PERMIT_PACKAGE_CDROM =	No
PERMIT_PACKAGE_FTP =	Yes

WANTLIB =		c crypto pthread ssl z

# packaged from git://git.ffmpeg.org/rtmpdump : dc76f0a846
MASTER_SITES =		http://spacehopper.org/mirrors/

MAKE_FLAGS =		CC="${CC}" XCFLAGS="${CFLAGS}" VERSION=${RVER} OPT= \
			THREADLIB=-pthread SO_VERSION=${LIBrtmp_VERSION}

NO_TEST =		Yes

post-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/rtmpdump
	cd ${WRKBUILD}; \
	  ${INSTALL_DATA} README COPYING ChangeLog ${PREFIX}/share/doc/rtmpdump

.include <bsd.port.mk>
