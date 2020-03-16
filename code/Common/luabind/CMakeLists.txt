fips_begin_module(luabind)
fips_src(src)
fips_deps(lua5.1)
fips_end_module()

fips_begin_module(luabind-test)
fips_src(test)
fips_deps(lua5.1)
fips_end_module()