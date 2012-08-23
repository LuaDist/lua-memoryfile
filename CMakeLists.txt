# Copyright (C) 2007-2012 LuaDist.
# Created by Peter Kapec
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.
# Please note that the package source code is licensed under its own license.

project ( lua_memoryfile C )
cmake_minimum_required ( VERSION 2.8 )
include ( cmake/dist.cmake )
include ( lua )

# Memoryfile
add_definitions ( -DVERSION="${DIST_VERSION}" )
install_lua_module ( memoryfile memoryfile.c memoryfile.def )
install_data ( COPYRIGHT Changes README )
install_doc ( doc/ )
install_test ( test/ memoryfile-test.lua lunit.lua )
