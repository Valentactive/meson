# Comment on the first line
project('trivial test',
  # Comment inside a function call + array for language list
  ['c'],
  meson_version : '>=0.27.0')
#this is a comment
sources = 'trivial.c'

if meson.get_compiler('c').get_id() == 'intel'
  # Error out if the -std=xxx option is incorrect
  add_project_arguments('-diag-error', '10159', language : 'c')
endif

if meson.is_cross_build()
  native_exe = executable('native-trivialprog', sources : sources, native : true)
  test('native exe in cross build', native_exe)
endif

exe = executable('trivialprog', sources : sources)

test('runtest', exe) # This is a comment
