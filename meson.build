project('ImGui SDF', ['c', 'cpp'],
  version : '0.1',
  default_options : ['warning_level=3',
                     'cpp_std=c++20'])

dependencies = []
dependencies += dependency('sdl2')
dependencies += dependency('freetype2')
dependencies += dependency('gl')

incdirs = [] 
incdirs += include_directories('dependencies/imgui')

sources = []
# ImGui
sources += [
  'dependencies/imgui/imgui_demo.cpp',
  'dependencies/imgui/imgui_draw.cpp',
  'dependencies/imgui/imgui_impl_opengl3.cpp',
  'dependencies/imgui/imgui_impl_sdl2.cpp',
  'dependencies/imgui/imgui_tables.cpp',
  'dependencies/imgui/imgui_widgets.cpp',
  'dependencies/imgui/imgui.cpp',
  'dependencies/imgui/misc/freetype/imgui_freetype.cpp'
]

sources += 'src/main.cpp'

exe = executable(
  'demo',
  sources,
  include_directories: incdirs,
  dependencies: dependencies,
)

test('basic', exe)
