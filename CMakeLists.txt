# Copyright © 2024 Andy Maloney <asmaloney@gmail.com>
# SPDX-License-Identifier: MIT

project( rply
    LANGUAGES
        C
    VERSION
        1.1.4
)

message( STATUS "[${PROJECT_NAME}] version ${PROJECT_VERSION}" )

add_library( ${PROJECT_NAME} )

target_compile_features( ${PROJECT_NAME}
    PRIVATE
        c_std_90
)

target_sources( ${PROJECT_NAME}
	PRIVATE
	    rply.h
		rplyfile.h
		rply.c
)

target_include_directories( ${PROJECT_NAME} SYSTEM
    PUBLIC
        .
)
