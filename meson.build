project('SDL2_gfx', 'c')

cmake = import('cmake')

sdl_dep = dependency('sdl2', required : false)
if not sdl_dep.found()
    cmake_opt = cmake.subproject_options()
    cmake_opt.add_cmake_defines({'LIBC': true})
    sdl_proj = cmake.subproject('SDL', options : cmake_opt)
    sdl_dep = sdl_proj.dependency('SDL2')
endif

incdir = include_directories('.')

sdl_gfx_lib = library(
    'SDL_gfx',
    'SDL2_framerate.c',
    'SDL2_gfxPrimitives.c',
    'SDL2_imageFilter.c',
    'SDL2_rotozoom.c',
    include_directories : incdir,
    dependencies : sdl_dep
)

sdl_gfx_dep = declare_dependency(
    include_directories : incdir,
    link_with : sdl_gfx_lib
)

