project('mongoose', 'c')

mongoose_lib = library(
  'mongoose',
  sources: files(
    'mongoose.c',
    # the src/*.c files are not needed
    # they are included (#line 1 "src/foo.c")
  ),
  include_directories: [
    include_directories('.')
  ],
  c_args: [
    # https://github.com/cesanta/mongoose/blob/master/examples/desktop-server/Makefile
    # DEFS ?= -DMG_ENABLE_LINES=1 -DMG_ENABLE_DIRECTORY_LISTING=1
    # CFLAGS ?= -I../.. -W -Wall -DMG_ENABLE_IPV6=1 $(DEFS) $(EXTRA)
    # '-DMG_ENABLE_LOG=1',
    # '-DMG_ENABLE_FS',
    '-DMG_ENABLE_DIRECTORY_LISTING=1',
    # '-DMG_ENABLE_LINES=1',
    # '-DMG_ENABLE_IPV6=1',
    # '-W',
    # '-Wall',
    ]
)
mongoose_dep = declare_dependency(
  link_with: mongoose_lib,
  include_directories: include_directories('.'),
)
