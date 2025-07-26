# SPDX-License-Identifier: CC0-1.0

libcamera_internal_sources += files([
    'pisp.cpp',
])

librt = cc.find_library('rt', required : true)

pisp_libdir = get_option('libpisp-libdir')
pisp_incdir = get_option('libpisp-includedir')

libpisp_dep = declare_dependency(link_args : ['-L' + pisp_libdir, '-llibpisp'],
                               include_directories : [pisp_incdir])

libcamera_deps += [libpisp_dep, librt]

subdir('data')
