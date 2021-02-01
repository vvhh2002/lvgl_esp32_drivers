if(ESP_PLATFORM)

file(GLOB SOURCES *.c)

idf_component_register(SRCS ${SOURCES}
                       INCLUDE_DIRS .
                       REQUIRES lvgl)
target_compile_definitions(${COMPONENT_TARGET} PUBLIC "-DLV_LVGL_H_INCLUDE_SIMPLE")
endif()
