fips_begin_app(cpp_using_lua cmdline)
    fips_files_ex(cpp_using_lua *.cpp GROUP "Source Files")

    fips_include_directories(../Common/lua-5.1.3/include)
    fips_deps(lua5.1)
fips_end_app()

fips_begin_app(lua_using_cpp cmdline)
    fips_include_directories(../Common/luabind)
    include_directories($ENV{BOOST_1_72_INCLUDE_PATH})
    link_directories($ENV{BOOST_1_72_LINK_PATH})
    
    fips_files_ex(lua_using_cpp *.cpp GROUP "Source Files")
    fips_files_ex(lua_using_cpp *.h GROUP "Header Files")
    fips_files_ex(lua_using_cpp *.lua GROUP "lua scripts")
    
    fips_include_directories(../Common/lua-5.1.3/include)
    fips_deps(lua5.1)
fips_end_app()

fips_begin_app(CreatingClassesUsingLuaBind cmdline)
    fips_include_directories(../Common/luabind)
    include_directories($ENV{BOOST_1_72_INCLUDE_PATH})
    link_directories($ENV{BOOST_1_72_LINK_PATH})

    fips_files_ex(lua_using_cpp *.cpp GROUP "Source Files")
    fips_files_ex(lua_using_cpp *.h GROUP "Header Files")
    fips_files_ex(lua_using_cpp *.lua GROUP "lua scripts")
    
    fips_include_directories(../Common/lua-5.1.3/include)
    fips_deps(lua5.1)
fips_end_app()

fips_begin_app(ExposingCPPClassesUsingLuaBind cmdline)
    fips_include_directories(../Common/luabind)
    include_directories($ENV{BOOST_1_72_INCLUDE_PATH})
    link_directories($ENV{BOOST_1_72_LINK_PATH})

    fips_files_ex(lua_using_cpp *.cpp GROUP "Source Files")
    fips_files_ex(lua_using_cpp *.h GROUP "Header Files")
    fips_files_ex(lua_using_cpp *.lua GROUP "lua scripts")
    
    fips_include_directories(../Common/lua-5.1.3/include)
    fips_deps(lua5.1)
fips_end_app()

fips_begin_app(ExposingCPPFunctionsToLua cmdline)
    fips_include_directories(../Common/luabind)
    include_directories($ENV{BOOST_1_72_INCLUDE_PATH})
    link_directories($ENV{BOOST_1_72_LINK_PATH})

    fips_files_ex(ExposingCPPFunctionsToLua *.cpp GROUP "Source Files")
    
    fips_include_directories(../Common/lua-5.1.3/include)
    fips_deps(lua5.1)
fips_end_app()

fips_begin_app(ScriptedStateMachine cmdline)
    fips_include_directories(../Common/luabind)
    include_directories($ENV{BOOST_1_72_INCLUDE_PATH})
    link_directories($ENV{BOOST_1_72_LINK_PATH})

    fips_files_ex(ScriptedStateMachine *.cpp GROUP "Source Files")
    fips_files_ex(ScriptedStateMachine *.h GROUP "Header Files")
    fips_files_ex(ScriptedStateMachine *.lua GROUP "lua scripts")
    
    fips_include_directories(../Common/lua-5.1.3/include)
    fips_deps(lua5.1)
fips_end_app()

fips_begin_app(StartHere cmdline)
    fips_files_ex(StartHere *.cpp GROUP "Source Files")
    fips_files_ex(StartHere *.lua GROUP "lua scripts")
    
    fips_include_directories(../Common/lua-5.1.3/include)
    fips_deps(lua5.1)
fips_end_app()