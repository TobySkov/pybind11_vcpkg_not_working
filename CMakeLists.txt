cmake_minimum_required (VERSION 3.19)

project (project_name)

find_package(pybind11 CONFIG REQUIRED)
#find_package(Python3 REQUIRED COMPONENTS Interpreter Development)

pybind11_add_module(simple_python src/simple_binding.cpp)

target_link_libraries(simple_python PRIVATE pybind11::lto pybind11::embed pybind11::module)
#target_link_libraries(simple_python PRIVATE Python3::Python)

