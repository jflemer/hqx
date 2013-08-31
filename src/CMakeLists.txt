cmake_minimum_required(VERSION 2.8)
add_definitions(-DDLL_EXPORT)
set(HQX_SOURCES
	common.c
	hq2x.c
	hq3x.c
	hq4x.c
	init.c)
set(HQX_HEADERS
	common.h
	hqx.h)
add_library(hqx SHARED ${HQX_SOURCES} ${HQX_HEADERS})
if(MSVC)
	set_target_properties(hqx PROPERTIES RUNTIME_OUTPUT_DIRECTORY ..)
	set_target_properties(hqx PROPERTIES RUNTIME_OUTPUT_DIRECTORY_DEBUG ..)
	set_target_properties(hqx PROPERTIES RUNTIME_OUTPUT_DIRECTORY_RELEASE ..)
endif(MSVC)
