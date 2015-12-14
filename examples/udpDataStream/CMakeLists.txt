cmake_minimum_required(VERSION 2.8)
project (uip_examples)

include(${ARDUINO_SETTINGS_FILE})
 
set(PROJECT_INCLUDE_DIR ${CMAKE_SOURCE_DIR}/include)
 
include_directories("${PROJECT_BINARY_DIR}")
include_directories("${PROJECT_INCLUDE_DIR}")

### add example executable directories
add_avr_executable(uip_udpDataStream_test udpDataStream.cpp)
### add the dependant libraries
avr_target_link_libraries(uip_udpDataStream_test UIPETHERNET)
avr_target_link_libraries(uip_udpDataStream_test ARDUINO)
