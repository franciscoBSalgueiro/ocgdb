add_library(SQLiteCpp STATIC
    Assertion.h
    Backup.cpp
    Backup.h
    Column.cpp
    Column.h
    Database.cpp
    Database.h
    Exception.cpp
    Exception.h
    ExecuteMany.h
    Savepoint.cpp
    Savepoint.h
    SQLiteCpp.h
    Statement.cpp
    Statement.h
    Transaction.cpp
    Transaction.h
    Utils.h
    VariadicBind.h
)
target_include_directories(SQLiteCpp PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)
target_link_libraries(SQLiteCpp PUBLIC sqlite3)