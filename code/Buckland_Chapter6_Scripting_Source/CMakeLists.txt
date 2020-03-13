fips_begin_module(cpp_using_lua)
    link_directories(../Common/lua-5.1.3)
    fips_include_directories(../Common/lua-5.1.3/include)

    fips_files_ex(cpp_using_lua *.cpp GROUP "Source Files")
    fips_files_ex(cpp_using_lua *.h GROUP "Header Files")
    fips_files_ex(cpp_using_lua *.lua GROUP "lua scripts")
    fips_libs(lua5.1.lib)
fips_end_module()