fips_begin_app(cpp_using_lua cmdline)
    fips_files_ex(cpp_using_lua *.cpp GROUP "Source Files")
    # fips_files_ex(cpp_using_lua *.h GROUP "Header Files")
    fips_files_ex(cpp_using_lua *.lua GROUP "lua scripts")

    fips_include_directories(../Common/lua-5.1.3/include)
    fips_deps(lua5.1)

    ## this .ini is the config file for runtime program
    file( COPY ${CMAKE_CURRENT_SOURCE_DIR}/cpp_using_lua/cpp_using_lua.lua DESTINATION ${FIPS_PROJECT_DEPLOY_DIR} )
fips_end_app()

fips_begin_app(lua_using_cpp cmdline)
    fips_files_ex(lua_using_cpp *.cpp GROUP "Source Files")
    fips_files_ex(lua_using_cpp *.h GROUP "Header Files")
    fips_files_ex(lua_using_cpp *.lua GROUP "lua scripts")
    
    fips_deps(lua5.1)

    ## this .ini is the config file for runtime program
    file( COPY ${CMAKE_CURRENT_SOURCE_DIR}/lua_using_cpp/Rock_Paper_Scissors_Using_C++_Funcs.lua DESTINATION ${FIPS_PROJECT_DEPLOY_DIR} )
fips_end_app()

fips_begin_app(CreatingClassesUsingLuaBind cmdline)
    fips_files_ex(CreatingClassesUsingLuaBind *.cpp GROUP "Source Files")
    # fips_files_ex(CreatingClassesUsingLuaBind *.h GROUP "Header Files")
    fips_files_ex(CreatingClassesUsingLuaBind *.lua GROUP "lua scripts")
    
    fips_deps(luabind)

    ## this .ini is the config file for runtime program
    file( COPY ${CMAKE_CURRENT_SOURCE_DIR}/CreatingClassesUsingLuaBind/classes_in_lua.lua DESTINATION ${FIPS_PROJECT_DEPLOY_DIR} )
fips_end_app()

fips_begin_app(ExposingCPPClassesUsingLuaBind cmdline)
    fips_files_ex(ExposingCPPClassesUsingLuaBind *.cpp GROUP "Source Files")
    fips_files_ex(ExposingCPPClassesUsingLuaBind *.h GROUP "Header Files")
    fips_files_ex(ExposingCPPClassesUsingLuaBind *.lua GROUP "lua scripts")
    
    fips_deps(luabind)

    ## this .ini is the config file for runtime program
    file( COPY ${CMAKE_CURRENT_SOURCE_DIR}/ExposingCPPClassesUsingLuaBind/ExposingCPPClassesToLua.lua DESTINATION ${FIPS_PROJECT_DEPLOY_DIR} )
fips_end_app()

fips_begin_app(ExposingCPPFunctionsToLua cmdline)
    fips_files_ex(ExposingCPPFunctionsToLua *.cpp GROUP "Source Files")
    
    include_directories($ENV{BOOST_1_48_0_INCLUDE_PATH})
    fips_include_directories(../Common/luabind)
    fips_deps(luabind)

    ## this .ini is the config file for runtime program
    file( COPY ${CMAKE_CURRENT_SOURCE_DIR}/ExposingCPPFunctionsToLua/ExposingCPPFunctionsToLua.lua DESTINATION ${FIPS_PROJECT_DEPLOY_DIR} )
fips_end_app()

fips_begin_app(ScriptedStateMachine cmdline)
    fips_files_ex(ScriptedStateMachine *.cpp GROUP "Source Files")
    fips_files_ex(ScriptedStateMachine *.h GROUP "Header Files")
    fips_files_ex(ScriptedStateMachine *.lua GROUP "lua scripts")
    
    include_directories($ENV{BOOST_1_48_0_INCLUDE_PATH})
    fips_include_directories(../Common/luabind)
    fips_deps(luabind)

    ## this .ini is the config file for runtime program
    file( COPY ${CMAKE_CURRENT_SOURCE_DIR}/ScriptedStateMachine/StateMachineScript.lua DESTINATION ${FIPS_PROJECT_DEPLOY_DIR} )
fips_end_app()

fips_begin_app(StartHere cmdline)
    fips_files_ex(StartHere *.cpp GROUP "Source Files")
    fips_files_ex(StartHere *.lua GROUP "lua scripts")
    
    fips_include_directories(../Common/luabind)
    fips_deps(luabind)

    ## this .ini is the config file for runtime program
    file( COPY ${CMAKE_CURRENT_SOURCE_DIR}/StartHere/your_first_lua_script.lua DESTINATION ${FIPS_PROJECT_DEPLOY_DIR} )
fips_end_app()