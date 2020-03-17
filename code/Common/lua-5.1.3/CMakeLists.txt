
fips_begin_module(lua5.1)
fips_include_directories(include)
fips_include_directories(src)
fips_files_ex(include *.h *.hpp GROUP "Header Files")
fips_files_ex(src *.h GROUP "Header Files")
fips_files_ex(src *.c EXCEPT lua.c luac.c GROUP "Source Files")
fips_end_module()