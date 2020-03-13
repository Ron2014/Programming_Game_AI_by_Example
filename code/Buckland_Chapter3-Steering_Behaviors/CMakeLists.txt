fips_begin_module(Steering)
    fips_files_ex(. *.cpp GROUP "Source Files")
    fips_files_ex(. *.h EXCEPT resource.h GROUP "Header Files")

    fips_dir(. GROUP "Resource files")
    fips_files(
        params.ini
        resource.h
        Script1.rc
    )

    fips_deps(Misc)
fips_end_module()