# personal c++ project template

- use meson & ninja
- use clang-format
- std = c++17
- dependencies[^fn#1]
  - libfmt for c++20 sytle fmt
  - spdlog for log
  - gtest for utest
  - nlohmann_json for json prasing and writing

Run `runme` to set project name.

[^fn#1]: If we cannot find dependencies in system, this meson.build will
  fallback to download and build them using `meson wrap`.
