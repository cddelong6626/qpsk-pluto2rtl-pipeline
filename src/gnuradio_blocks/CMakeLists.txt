file(GLOB GNURADIO_SOURCES *.cpp)
add_library(gr_blocks STATIC ${GNURADIO_SOURCES})
target_include_directories(gr_blocks PUBLIC ${CMAKE_SOURCE_DIR}/include)

# Link to DSP
target_link_libraries(gr_blocks dsp)
