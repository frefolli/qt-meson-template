project('temp', 'cpp',
        version : '0.1',
        default_options : ['warning_level=3',
                           'cpp_std=c++20'])

qt6 = import('qt6')
libQt6 = dependency('qt6', modules : 'Widgets')

processed = qt6.preprocess(
  moc_headers : './include/window.hpp',
)

includes = include_directories('./include')
main = executable('main.exe', [
    './src/main.cpp',
    './src/window.cpp',
    processed
  ], include_directories: includes,
  dependencies: [libQt6])
