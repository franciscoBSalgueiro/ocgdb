add_library(board STATIC 
    base.cpp
    base.h
    chess.cpp
    chess.h
    chesstypes.cpp
    chesstypes.h
    funcs.cpp
    funcs.h
    types.h
)
target_include_directories(board PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})