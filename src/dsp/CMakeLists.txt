file(GLOB DSP_SOURCES *.cpp)
add_library(dsp STATIC ${DSP_SOURCES})
target_include_directories(dsp PUBLIC ${CMAKE_SOURCE_DIR}/include)
