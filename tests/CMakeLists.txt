
FetchContent_Declare(
	catch
	GIT_REPOSITORY https://github.com/catchorg/Catch2.git
	GIT_TAG v3.3.1)
FetchContent_MakeAvailable(catch)

add_executable(testlib testlib.cpp)

target_compile_features(testlib PIRVATE cxx_std_14)

target_link_libraries(testlib PRIVATE pjaat_library Catch2::Catch2)

# add_test(NAME testlibtest COMMAND testlib) # Command can be a target
