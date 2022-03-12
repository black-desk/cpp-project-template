project(
  '[[[project_name]]]',
  'cpp',
  default_options : [
    'warning_level=3',
    'werror=true',
    'cpp_std=c++17',
  ],
  license : 'GPL-3.0-only',
)

dep_list = {
  'fmt': 'fmt_dep',
  'nlohmann_json': 'nlohmann_json_dep',
  'spdlog': 'spdlog_dep',
}
deps = []
foreach dep_name, var_name: dep_list
  d = dependency(dep_name, required : false)
  if not d.found()
    d = subproject(dep_name).get_variable(var_name)
  endif
  deps += d
endforeach

incdir = include_directories('include')

subdir('lib')
subdir('src')
subdir('tests')
subdir('include/[[[project_name]]]')
