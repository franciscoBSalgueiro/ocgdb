cmake_minimum_required(VERSION 3.10)

project(ocgdb)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_subdirectory(board)
add_subdirectory(3rdparty/SQLiteCpp)
add_subdirectory(3rdparty/sqlite3)

add_executable(ocgdb main.cpp)
target_sources(ocgdb PRIVATE addgame.cpp addgame.h builder.cpp builder.h core.cpp core.h dbcore.cpp dbcore.h dbread.cpp duplicate.cpp duplicate.h epdbuilder.cpp exporter.cpp exporter.h extract.cpp extract.h main.cpp parser.cpp parser.h pgnread.cpp pgnread.h records.cpp records.h report.cpp report.h search.cpp search.h)
target_link_libraries(ocgdb PRIVATE board SQLiteCpp sqlite3)