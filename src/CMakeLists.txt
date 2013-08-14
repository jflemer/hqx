add_definitions(-DDLL_EXPORT)
set(HQX_SOURCES
	hq2x.c
	hq3x.c
	hq4x.c
	init.c)
set(HQX_HEADERS
	common.h
	hqx.h)
add_library(hqx SHARED ${HQX_SOURCES} ${HQX_HEADERS})