# personal c++ project template

- use meson & ninja
- use clang-format
- std = c++17
- deps
  - libfmt for c++20 sytle fmt
  - spdlog for log
  - gtest for utest
  - nlohmann_json for json prasing and writing

If we cannot find dependencies in system, download and build them using `meson 
wrap`.

Run `runme` to set project name.
