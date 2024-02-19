cmake_minimum_required(VERSION 3.12)

project(18.vcpkg_example)

add_executable(format format.cpp)

set_target_properties(format 
	PROPERTIES CXX_STANDARD 17 
	CXX_STANDARD_REQUIRED ON
)

find_package(fmt CONFIG REQUIRED)

#target_link_libraries(format PRIVATE fmt::fmt)

target_link_libraries(format 
	PRIVATE 
	fmt::fmt 
	#fmt::fmt-header-only
)