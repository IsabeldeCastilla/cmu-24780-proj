file(GLOB DEMO_SOURCES "demo*")
message(STATUS "demo > DEMO_SOURCES: ${DEMO_SOURCES}")

add_executable(demo MACOSX_BUNDLE ${DEMO_SOURCES} ${FSSIMPLE_SOURCES} ${FSSIMPLE_HEADER} ${SIMPLESOUND_HEADER} ${SIMPLESOUND_SOURCES} ${BITMAP_FONT_HEADER} ${BITMAP_FONT_SOURCES})
target_link_libraries(demo ${COCOA_LIBRARY} ${OGL_LIBRARY} ${AVFOUNDATION_FRAMEWORK})
copy_resources(demo)