gtest = dependency('gtest', main : true, required : false, method : 'system')
if not gtest.found()
  gtest_proj = subproject('gtest')
  gtest = gtest_proj.get_variable('gtest_dep')
  gmock = gtest_proj.get_variable('gmock_dep')
else
  gmock = dependency('gmock', required : false)
endif

tests = [
  'hello',
]

tests_deps = [
  gtest,
  gmock,
]

tests_deps += deps

foreach t : tests
  src = [
    t + '/test.cpp',
  ]

  exe = executable(
    t,
    src,
    dependencies : tests_deps,
    link_with : [
      lib[[[project_name]]],
    ],
    include_directories : incdir,
  )

  test('gtest '+t, exe, is_parallel : true)
endforeach
