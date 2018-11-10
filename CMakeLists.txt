cmake_minimum_required(VERSION 2.8)

project(BattleCity)

set (CMAKE_CXX_STANDARD 11)
set(CMAKE_MODULE_PATH "/usr/share/SFML/cmake/Modules/;${CMAKE_MODULE_PATH}")
find_package(SFML 2 REQUIRED COMPONENTS network audio graphics window system)

set(SOURCES
    main.cpp
    src/Animation.h
    src/Bonus.h
    src/Bullet.h
    src/Category.h
    src/Entity.h
    src/Game.h
    src/Map.h
    src/Player.h
    src/ResourceHolder.h
    src/RightPanel.h
    src/StringHelpers.h
    src/Tank.h
    src/private/Animation.cpp
    src/private/Bonus.cpp
    src/private/Bullet.cpp
    src/private/Entity.cpp
    src/private/Game.cpp
    src/private/Map.cpp
    src/private/Player.cpp
    src/private/ResourceHolder.cpp
    src/private/RightPanel.cpp
    src/private/Tank.cpp
)
add_executable(${PROJECT_NAME} ${SOURCES})
target_link_libraries(${PROJECT_NAME} ${SFML_LIBRARIES} ${SFML_DEPENDENCIES})

