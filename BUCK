include_defs('//BUCKAROO_DEPS')

bzip2 = read_config('boost.iostreams', 'bzip2', False)
zlib = read_config('boost.iostreams', 'zlib', False)

cxx_library(
  name = 'iostreams',
  header_namespace = 'boost/iostreams',
  exported_headers = subdir_glob([
    ('include/boost/iostreams', '**/*.hpp'),
  ]),
  srcs = glob([
    'src/**/*.cpp',
  ], excludes = [
    'src/bzip2.cpp', 
    'src/zlib.cpp', 
  ]) + (
    [ 'src/bzip2.cpp' ] if bzip2 else []
  ) + (
    [ 'src/zlib.cpp' ] if zlib else []
  ),
  visibility = [
    'PUBLIC',
  ],
  deps = BUCKAROO_DEPS,
)
