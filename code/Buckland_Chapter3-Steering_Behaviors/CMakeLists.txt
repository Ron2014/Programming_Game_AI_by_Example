fips_begin_app(Steering windowed)
    fips_vs_warning_level(3)
    fips_files_ex(. *.cpp GROUP "Source Files")
    fips_files_ex(. *.h EXCEPT resource.h GROUP "Header Files")

    fips_dir(../Common GROUP "misc")
    fips_files(
        misc/utils.h
        misc/Cgdi.h misc/Cgdi.cpp
        misc/iniFileLoaderBase.h misc/iniFileLoaderBase.cpp
        misc/Stream_Utility_Functions.h
        misc/WindowUtils.h misc/WindowUtils.cpp
        misc/Smoother.h
    
        Time/PrecisionTimer.h Time/PrecisionTimer.cpp
    
        2D/C2DMatrix.h
        2D/geometry.h
        2D/Transformations.h
        2D/Vector2D.h 2D/Vector2d.cpp
        2D/Wall2D.h
        
        Game/EntityFunctionTemplates.h
    )

    fips_dir(. GROUP "Resource files")
    fips_files(
        Steering-params.ini
        resource.h
        Script1.rc
    )
    
    ## this .ini is the config file for runtime program
    file( COPY ${CMAKE_CURRENT_SOURCE_DIR}/Steering-params.ini DESTINATION ${FIPS_PROJECT_DEPLOY_DIR} )
fips_end_app()