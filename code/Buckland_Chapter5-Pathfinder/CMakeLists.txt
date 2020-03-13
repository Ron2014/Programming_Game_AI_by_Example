fips_begin_app(Pathfinder windowed)
    fips_dir(../Common GROUP "common")
    fips_files(
        misc/utils.h
        misc/Cgdi.h misc/Cgdi.cpp
        misc/PriorityQueue.h
        misc/Stream_Utility_Functions.h
        misc/WindowUtils.h misc/WindowUtils.cpp

        Time/PrecisionTimer.h Time/PrecisionTimer.cpp

        2D/Vector2D.h 2D/Vector2d.cpp
    )

    fips_src(../Common/Graph GROUP "graph related files")

    fips_dir(. GROUP "Header Files")
    fips_files(
        constants.h
        Pathfinder.h
    )
    
    fips_dir(. GROUP "Source Files")
    fips_files(
        main.cpp
        Pathfinder.cpp
    )
    
    fips_dir(. GROUP "Resource Files")
    fips_files(
        icon1.ico
        resource.h
        toolbar.rc
        toolbar1.bmp
    )
fips_end_app()