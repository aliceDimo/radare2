files = [
  'flag.c',
  'sort.c',
  'spaces.c',
  'zones.c'
]

r_flag = library('r_flag', files,
  include_directories: [platform_inc],
  link_with: [r_util, libr_shlr],
  install: true,
  implicit_include_directories: false
)


pkg = import('pkgconfig')
pkg.generate(libraries: [r_flag],
             subdirs: 'libr',
             version: r2version,
             name: 'r_flag',
             filebase: 'r_flag',
             requires: [
               'r_util'
             ],
             description: 'radare foundation libraries')
