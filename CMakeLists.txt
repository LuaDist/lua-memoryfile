# Copyright (C) 2007-2009 LuaDist.
# Created by Peter Kapec
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.
# Please note that the package source code is licensed under its own license.

PROJECT(lua_memoryfile C)
CMAKE_MINIMUM_REQUIRED(VERSION 2.6)
INCLUDE(dist.cmake)

# Memmoryfile
ADD_DEFINITIONS(-DVERSION="1.0")
ADD_LUA_MODULE(memoryfile  memoryfile.c memoryfile.def)

# Install all files and documentation
INSTALL (TARGETS memoryfile DESTINATION ${INSTALL_CMOD})
INSTALL (FILES COPYRIGHT Changes README DESTINATION ${INSTALL_DATA})
INSTALL (DIRECTORY doc DESTINATION ${INSTALL_DATA})
INSTALL (DIRECTORY test DESTINATION ${INSTALL_DATA})
INSTALL (FILES memoryfile-test.lua lunit.lua DESTINATION ${INSTALL_TEST})
