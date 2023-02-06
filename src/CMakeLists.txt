set(HEADER_LIST "${pjaat_SOURCE_DIR}/include/pjaat/lib.hpp")

add_library(pjaat_library lib.cpp ${HEADER_LIST})

target_include_directories(pjaat_library PUBLIC ../include)

#target_link_libraries(pjaat_library PRIVAETE BOOST:boost)

target_compile_features(pjaat_library PUBLIC cxx_std_14)

