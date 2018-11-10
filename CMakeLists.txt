cmake_minimum_required(VERSION 2.8)

project(BattleCity)

set (CMAKE_CXX_STANDARD 11)
set(CMAKE_MODULE_PATH "/usr/share/SFML/cmake/Modules/;${CMAKE_MODULE_PATH}")
find_package(SFML 2 REQUIRED COMPONENTS network audio graphics window system)

set(SOURCES
    main.cpp
    Headers/Animation.h
    Animation.cpp
    Headers/Bonus.h
    Bonus.cpp
    Headers/Bullet.h
    Bullet.cpp
    Headers/Category.h
    Headers/Entity.h
    Entity.cpp
    Headers/Game.h
    Game.cpp
    Headers/Map.h
    Map.cpp
    Headers/Player.h
    Player.cpp
    Headers/ResourceHolder.h
    ResourceHolder.cpp
    Headers/RightPanel.h
    RightPanel.cpp
    Headers/StringHelpers.h
    Headers/Tank.h
    Tank.cpp
)
add_executable(${PROJECT_NAME} ${SOURCES})
target_link_libraries(${PROJECT_NAME} ${SFML_LIBRARIES} ${SFML_DEPENDENCIES})

