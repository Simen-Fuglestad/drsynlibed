cmake_minimum_required(VERSION 3.10)

project	(pjaat	VERSION 	0.1
		DESCRIPTION	"Digital Synthesizer Engine"	
		LANGUAGES	C CXX
	)

if (CMAKE_PROJECT_NAME STREQUAL PROJECT_NAME)

	set(CMAKE_CXX_STANDARD 14)
	set(CMAKE_CXX_STANDARD_REQUIRED True)
endif()

add_subdirectory(src)

add_subdirectory(apps)

if((CMAKE_PROJECT_NAME STREQUAL PROJECT_NAME OR MODERN_CMAKE_BUILD_TESTING)
		AND BUILD_TESTING)
	add_subdirectory(tests)
endif()
