fips_begin_app(Raven windowed)

fips_files_ex(../Common/fuzzy Fuzzy*.* EXCEPT FuzzySet*.* GROUP "AI/fuzzy logic")
fips_files_ex(../Common/fuzzy FuzzySet*.* GROUP "AI/fuzzy logic/fuzzy set types")

fips_files_ex(./goals Raven_Goal_Types.h Raven_Goal_Types.cpp GROUP "AI/goals")

fips_files_ex(../Common/Goals Goal.h GROUP "AI/goals/atomic")
fips_dir(./goals GROUP "AI/goals/atomic")
fips_files(
    Goal_DodgeSideToSide.h Goal_DodgeSideToSide.cpp
    Goal_SayPhrase.cpp
    # Goal_SayPhrase.h Goal_SayPhrase.cpp
    Goal_SeekToPosition.h Goal_SeekToPosition.cpp
    Goal_TraverseEdge.h Goal_TraverseEdge.cpp
    Goal_Wander.h Goal_Wander.cpp   
)


fips_files_ex(../Common/Goals Goal_Composite.h GROUP "AI/goals/composite")
fips_dir(./goals GROUP "AI/goals/composite")
fips_files(
    Goal_AdjustRange.h Goal_AdjustRange.cpp
    Goal_AttackTarget.h Goal_AttackTarget.cpp
    Goal_Explore.h Goal_Explore.cpp
    Goal_FollowPath.h Goal_FollowPath.cpp
    Goal_GetItem.h Goal_GetItem.cpp
    Goal_HuntTarget.h Goal_HuntTarget.cpp
    Goal_MoveToPosition.h Goal_MoveToPosition.cpp
    Goal_NegotiateDoor.h Goal_NegotiateDoor.cpp
    Goal_Think.h Goal_Think.cpp
)

fips_dir(./goals GROUP "AI/goals/goal evaluation")
fips_files(
    AttackTargetGoal_Evaluator.h AttackTargetGoal_Evaluator.cpp
    ExploreGoal_Evaluator.h ExploreGoal_Evaluator.cpp
    GetHealthGoal_Evaluator.h GetHealthGoal_Evaluator.cpp
    GetWeaponGoal_Evaluator.h GetWeaponGoal_Evaluator.cpp
    Raven_Feature.h Raven_Feature.cpp
    Goal_Evaluator.h
)

fips_src(../Common/Messaging GROUP "AI/Messaging")
fips_files_ex(. Raven_Messages.h GROUP "AI/Messaging")

fips_src(../Common/Graph GROUP "AI/Movement & Navigation")
fips_files_ex(../Common/misc CellSpacePartition.h GROUP "AI/Movement & Navigation")
fips_src(./navigation GROUP "AI/Movement & Navigation")

fips_files_ex(. Raven_SensoryMemory.h Raven_SensoryMemory.cpp GROUP "AI/Sensory Memory")
fips_files_ex(. Raven_TargetingSystem.h Raven_TargetingSystem.cpp GROUP "AI/Target Selection")

fips_src(../Common/Triggers GROUP "AI/Triggers")
fips_src(./triggers GROUP "AI/Triggers")

fips_files_ex(. Raven_WeaponSystem.h Raven_WeaponSystem.cpp GROUP "AI/Weapon Handling")

fips_dir(../Common GROUP "Common")
fips_files(
    misc/utils.h
    misc/Cgdi.h misc/Cgdi.cpp
    misc/FrameCounter.h misc/FrameCounter.cpp
    misc/PriorityQueue.h
    misc/Stream_Utility_Functions.h
    misc/WindowUtils.h misc/WindowUtils.cpp

    Time/PrecisionTimer.h Time/PrecisionTimer.cpp
    Time/CrudeTimer.h Time/CrudeTimer.cpp
    Time/Regulator.h

    2D/C2DMatrix.h
    2D/geometry.h
    2D/Transformations.h
    2D/Vector2D.h 2D/Vector2d.cpp
    2D/Wall2D.h
    2D/InvertedAABBox2D.h
    2D/WallIntersectionTests.h
    
    Debug/DebugConsole.h Debug/DebugConsole.cpp
)

fips_dir(. GROUP "Game")
fips_files(
    main.cpp
    Raven_Bot.h Raven_Bot.cpp
    Raven_Game.h Raven_Game.cpp
    Raven_Map.h Raven_Map.cpp
)

fips_dir(../Common/Game GROUP "Game/Base entity classes")
fips_files(
    BaseGameEntity.h BaseGameEntity.cpp
    EntityFunctionTemplates.h MovingEntity.h
    )

fips_dir(. GROUP "Game/misc")
fips_files(
    constants.h
    GraveMarkers.h    GraveMarkers.cpp
    Raven_Door.h    Raven_Door.cpp
    Raven_ObjectEnumerations.h
    Raven_UserOptions.h Raven_UserOptions.cpp
    ../Common/Game/EntityManager.h ../Common/Game/EntityManager.cpp
)

fips_dir(. GROUP "Game/Script related")
fips_files(Params.lua)
fips_dir(./lua GROUP "Game/Script related/general")
fips_files(Raven_Scriptor.h Raven_Scriptor.cpp)
fips_files_ex(../Common/script Scriptor.h GROUP "Game/Script related/general")
fips_src(../Common/lua-5.1.3/include GROUP "Game/Script related/lua headers")

fips_dir(. GROUP "Game/weapons & projectiles")
fips_files_ex(./armory Projectile_*.* Raven_Projectile.* GROUP "Game/weapons & projectiles/projectiles")
fips_files_ex(./armory Weapon_*.* Raven_Weapon.* GROUP "Game/weapons & projectiles/weapons")

fips_dir(. GROUP "Resource Files")
fips_files(
    # note.txt
    resource.h
    Script1.rc
)

fips_dir(./maps GROUP "Resource Files/maps")
fips_files(
    Raven_DM1.map
    Raven_DM1_With_Doors.map
)

if(FIPS_WINDOWS)
    include_directories(../Common/lua-5.1.3/include)
    link_directories(../Common/lua-5.1.3)
    fips_libs(lua5.1.lib)
endif()

fips_end_app()
