# Copyright (C) 2007-2009 LuaDist.
# Created by Peter Kapec
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.
# Please note that the package source code is licensed under its own license.

PROJECT(lua_signal C)
CMAKE_MINIMUM_REQUIRED(VERSION 2.8)
INCLUDE(dist.cmake)

# Build
INCLUDE_DIRECTORIES(lua_signal-1.000.src)
ADD_LUA_MODULE(signal lsignal.c signal.def)

# Install all files and documentation
INSTALL (TARGETS signal DESTINATION ${INSTALL_CMOD})
INSTALL (FILES readme.txt DESTINATION ${INSTALL_DATA})
INSTALL (FILES test.lua DESTINATION ${INSTALL_TEST})
