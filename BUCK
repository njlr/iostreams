include_defs('//BUCKAROO_DEPS')

cxx_library(
  name = 'boost-iostreams',
  header_namespace = 'boost/iostreams',
  exported_headers = subdir_glob([
    ('include/boost/iostreams', '**/*.hpp'),
  ]),
  srcs = glob([
    'src/**/*.cpp',
  ]),
  visibility = [
    'PUBLIC',
  ],
  deps = BUCKAROO_DEPS,
)
