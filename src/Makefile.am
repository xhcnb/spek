bin_PROGRAMS = spek

spek_SOURCES = \
	spek.vala \
	spek-audio.c \
	spek-fft.c \
	spek-message-bar.vala \
	spek-pipeline.vala \
	spek-platform.c \
	spek-preferences.vala \
	spek-preferences-dialog.vala \
	spek-ruler.vala \
	spek-spectrogram.vala \
	spek-window.vala

AM_CPPFLAGS = \
	-include config.h \
	$(SPEK_CFLAGS) \
	$(IGE_MAC_CFLAGS) \
	-DLOCALEDIR=\""$(localedir)"\" \
	-DPKGDATADIR=\""$(pkgdatadir)"\" \
	-DPKGLIBDIR=\""$(pkglibdir)"\"

VALAFLAGS = \
	--thread \
	--vapidir=$(srcdir)/../vapi \
	--pkg config \
	--pkg spek-audio \
	--pkg spek-fft \
	--pkg spek-platform \
	@SPEK_PACKAGES@

spek_LDADD = \
	$(SPEK_LIBS) \
	$(IGE_MAC_LIBS)

EXTRA_DIST = \
	spek-audio.h \
	spek-fft.h \
	spek-platform.h
