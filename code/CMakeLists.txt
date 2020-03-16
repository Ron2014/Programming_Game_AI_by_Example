#
# project: BucklandAI
#
cmake_minimum_required(VERSION 2.8)
project(BucklandAI)
# include the fips main cmake file
get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
include("${FIPS_ROOT_DIR}/cmake/fips.cmake")

# include_directories(src)
fips_setup()

fips_include_directories(Common)

fips_ide_group(Common)
fips_add_subdirectory(Common)

fips_ide_group(Buckland_Chapter2-State_Machines)
fips_add_subdirectory(Buckland_Chapter2-State_Machines)

fips_ide_group(Buckland_Chapter3-Steering_Behaviors)
fips_add_subdirectory(Buckland_Chapter3-Steering_Behaviors)

fips_ide_group(Buckland_Chapter4-SimpleSoccer)
fips_add_subdirectory(Buckland_Chapter4-SimpleSoccer)

fips_ide_group(Buckland_Chapter5-Pathfinder)
fips_add_subdirectory(Buckland_Chapter5-Pathfinder)

fips_ide_group(Buckland_Chapter6_Scripting_Source)
fips_add_subdirectory(Buckland_Chapter6_Scripting_Source)

fips_ide_group(Buckland_Chapter7_to_10_Raven)
fips_add_subdirectory(Buckland_Chapter7_to_10_Raven)

fips_finish()


