# Copyright (C) 2019,2020 by Sukchan Lee <acetcom@gmail.com>

# This file is part of Open5GS.

# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU Affero General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <https://www.gnu.org/licenses/>.

libnas_common_sources = files('''
    types.c
    conv.c
    security.c
'''.split())

libnas_common_inc = include_directories('.')

libnas_common = library('ogsnas-common',
    sources : libnas_common_sources,
    version : libogslib_version,
    c_args : '-DOGS_NAS_COMPILATION',
    include_directories : [libnas_common_inc, libcrypt_inc, libinc],
    dependencies : libcrypt_dep,
    install : true)

libnas_common_dep = declare_dependency(
    link_with : libnas_common,
    include_directories : [libnas_common_inc, libcrypt_inc, libinc],
    dependencies : libcrypt_dep)
