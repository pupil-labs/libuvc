add_executable(test_enumerating_devices)
target_sources(test_enumerating_devices PRIVATE test-enumerating-devices.c)
target_link_libraries(test_enumerating_devices uvc)

add_test(NAME test_enumerating_devices COMMAND test_enumerating_devices)

add_executable(test_stream_timestamps)
target_sources(test_stream_timestamps PRIVATE test-stream-timestamps.c)
target_include_directories(
  test_stream_timestamps
  PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../include
)
target_link_libraries(test_stream_timestamps uvc)

add_test(NAME test_stream_timestamps COMMAND test_stream_timestamps)
