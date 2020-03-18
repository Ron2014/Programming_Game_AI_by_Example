

fips_begin_app(SimpleSoccer windowed)
    fips_dir(../Common GROUP "common")
    fips_files(
        misc/autolist.h
        misc/Cgdi.h misc/Cgdi.cpp
        misc/FrameCounter.h misc/FrameCounter.cpp
        misc/iniFileLoaderBase.h misc/iniFileLoaderBase.cpp
        misc/utils.h
        misc/WindowUtils.h misc/WindowUtils.cpp

        2D/C2DMatrix.h
        2D/geometry.h
        2D/Transformations.h
        2D/Vector2D.h 2D/Vector2d.cpp
        2D/Wall2D.h

        Time/PrecisionTimer.h Time/PrecisionTimer.cpp
        Time/Regulator.h

        Debug/DebugConsole.h Debug/DebugConsole.cpp
        Game/Region.h
    )

    fips_dir(../Common/Game GROUP "Entity related")
    fips_files(
        BaseGameEntity.h BaseGameEntity.cpp
        EntityFunctionTemplates.h
        EntityManager.h EntityManager.cpp
        MovingEntity.h
    )

    fips_dir(. GROUP "Entity related")
    fips_files(
        FieldPlayer.h FieldPlayer.cpp
        Goalkeeper.h Goalkeeper.cpp
        PlayerBase.h PlayerBase.cpp
        SoccerBall.h SoccerBall.cpp
    )

    fips_dir(../Common/Messaging GROUP "Messaging")
    fips_files(
        MessageDispatcher.h MessageDispatcher.cpp
        Telegram.h
    )

    fips_dir(. GROUP "Messaging")
    fips_files(
        SoccerMessages.h SoccerMessages.cpp
    )

    fips_dir(. GROUP "Header Files")
    fips_files(
        constants.h
        Goal.h
        ParamLoader.h
        SoccerPitch.h
        SoccerTeam.h
        SteeringBehaviors.h
        SupportSpotCalculator.h
    )

    fips_dir(. GROUP "Source Files")
    fips_files(
        main.cpp
        ParamLoader.cpp
        SoccerPitch.cpp
        SoccerTeam.cpp
        SteeringBehaviors.cpp
        SupportSpotCalculator.cpp
    )

    fips_dir(../Common/FSM GROUP "States and State Machine")
    fips_files(
        State.h StateMachine.h
    )

    fips_dir(. GROUP "States and State Machine")
    fips_files(
        FieldPlayerStates.h FieldPlayerStates.cpp
        GoalKeeperStates.h GoalKeeperStates.cpp
        TeamStates.h TeamStates.cpp
    )

    fips_dir(. GROUP "Resource Files")
    fips_files(
        icon1.ico
        SimpleSoccer-params.ini
        resource.h
        Script1.rc
    )

    ## this .ini is the config file for runtime program
    file( COPY ${CMAKE_CURRENT_SOURCE_DIR}/SimpleSoccer-params.ini DESTINATION ${FIPS_PROJECT_DEPLOY_DIR} )
fips_end_app()