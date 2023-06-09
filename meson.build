project('imgui test', 'cpp')


incdir = include_directories('/imgui/backends', '/imgui')

glfw_lib = subproject('glfw').get_variable('glfw_dep')
gl = dependency('gl')
dl = dependency('dl')

gui_files = files(
    'imgui_example.cpp',
    '/imgui/imgui.cpp',
    '/imgui/imgui_draw.cpp',
    '/imgui/imgui_tables.cpp',
    '/imgui/imgui_demo.cpp',
    '/imgui/imgui_widgets.cpp',
    '/imgui/backends/imgui_impl_glfw.cpp',
    '/imgui/backends/imgui_impl_opengl3.cpp',
    '/implot/implot.cpp',
    '/implot/implot_items.cpp'
)


executable('demo', gui_files, include_directories: incdir, dependencies: [glfw_lib, gl, dl])