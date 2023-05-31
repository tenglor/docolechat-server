cmake_minimum_required(VERSION 3.20.0 FATAL_ERROR)

project(docolechat-server)

add_executable(docolechat-server)

#find_package(Boost COMPONENTS asio REQUIRES)
#find_package(Boost REQUIRED)
find_package(Boost )

set(sources 
	src/main.cpp)

target_sources(docolechat-server PRIVATE ${sources})
#target_link_directories(docolechat-server PRIVATE Boost::asio)

target_link_directories(docolechat-server PRIVATE Boost::boost)
#target_link_directories(docolechat-server PRIVATE boost-http-server)