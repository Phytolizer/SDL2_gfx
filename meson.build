project('SDL2_gfx', 'c')

incdir = include_directories('.')

sdl_gfx_lib = library(
    'SDL_gfx',
    'SDL2_framerate.c',
    'SDL2_gfxPrimitives.c',
    'SDL2_imageFilter.c',
    'SDL2_rotozoom.c',
    include_directories : incdir
)

sdl_gfx_dep = declare_dependency(
    include_directories : incdir,
    link_with : sdl_gfx_lib
)

