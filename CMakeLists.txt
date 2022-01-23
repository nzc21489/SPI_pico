if (NOT TARGET spi)
    add_library(spi INTERFACE)

    target_sources(spi INTERFACE
            ${CMAKE_CURRENT_LIST_DIR}/Common.cpp
            ${CMAKE_CURRENT_LIST_DIR}/Print.cpp
            ${CMAKE_CURRENT_LIST_DIR}/SPI.cpp
            ${CMAKE_CURRENT_LIST_DIR}/Stream.cpp
            ${CMAKE_CURRENT_LIST_DIR}/String.cpp
    )

    target_link_libraries(spi INTERFACE hardware_spi)
endif()
