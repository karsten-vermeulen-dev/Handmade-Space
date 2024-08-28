cmake_minimum_required(VERSION 3.10)

project(Handmade)

set(CMAKE_CXX_STANDARD 17)

set(INCLUDE_FILES ${CMAKE_SOURCE_DIR}/src/App.h 
${CMAKE_SOURCE_DIR}/src/Audio.h
${CMAKE_SOURCE_DIR}/src/BoxCollider.h
${CMAKE_SOURCE_DIR}/src/Buffer.h
${CMAKE_SOURCE_DIR}/src/Camera.h
${CMAKE_SOURCE_DIR}/src/FreeCamera.h
${CMAKE_SOURCE_DIR}/src/Input.h
${CMAKE_SOURCE_DIR}/src/Material.h
${CMAKE_SOURCE_DIR}/src/Model.h
${CMAKE_SOURCE_DIR}/src/OBBCollider.h
${CMAKE_SOURCE_DIR}/src/Object.h
${CMAKE_SOURCE_DIR}/src/OrbitCamera.h
${CMAKE_SOURCE_DIR}/src/RigidBody.h
${CMAKE_SOURCE_DIR}/src/Screen.h
${CMAKE_SOURCE_DIR}/src/Shader.h
${CMAKE_SOURCE_DIR}/src/SphereCollider.h
${CMAKE_SOURCE_DIR}/src/State.h
${CMAKE_SOURCE_DIR}/src/Text.h
${CMAKE_SOURCE_DIR}/src/Texture.h
${CMAKE_SOURCE_DIR}/src/Tile.h
${CMAKE_SOURCE_DIR}/src/Transform.h
${CMAKE_SOURCE_DIR}/src/Utility.h)

set(SOURCE_FILES ${CMAKE_SOURCE_DIR}/src/App.cpp 
${CMAKE_SOURCE_DIR}/src/Audio.cpp
${CMAKE_SOURCE_DIR}/src/BoxCollider.cpp
${CMAKE_SOURCE_DIR}/src/Buffer.cpp
${CMAKE_SOURCE_DIR}/src/Camera.cpp
${CMAKE_SOURCE_DIR}/src/Design.cpp
${CMAKE_SOURCE_DIR}/src/FreeCamera.cpp
${CMAKE_SOURCE_DIR}/src/Input.cpp
${CMAKE_SOURCE_DIR}/src/Main.cpp
${CMAKE_SOURCE_DIR}/src/Material.cpp
${CMAKE_SOURCE_DIR}/src/Model.cpp
${CMAKE_SOURCE_DIR}/src/OBBCollider.cpp
${CMAKE_SOURCE_DIR}/src/Object.cpp
${CMAKE_SOURCE_DIR}/src/OrbitCamera.cpp
${CMAKE_SOURCE_DIR}/src/RigidBody.cpp
${CMAKE_SOURCE_DIR}/src/Screen.cpp
${CMAKE_SOURCE_DIR}/src/Shader.cpp
${CMAKE_SOURCE_DIR}/src/SphereCollider.cpp
${CMAKE_SOURCE_DIR}/src/Text.cpp
${CMAKE_SOURCE_DIR}/src/Texture.cpp
${CMAKE_SOURCE_DIR}/src/Tile.cpp
${CMAKE_SOURCE_DIR}/src/Transform.cpp
${CMAKE_SOURCE_DIR}/src/Utility.cpp
${CMAKE_SOURCE_DIR}/src/GLAD/gl.c)

set(SHADER_FILES ${CMAKE_SOURCE_DIR}/Shaders/Main.frag
${CMAKE_SOURCE_DIR}/Shaders/Main.vert)

add_executable(Handmade ${SOURCE_FILES} ${INCLUDE_FILES} ${SHADER_FILES})

target_include_directories(Handmade PRIVATE ${CMAKE_SOURCE_DIR}/src/FMOD)
target_include_directories(Handmade PRIVATE ${CMAKE_SOURCE_DIR}/src/FreeType)
target_include_directories(Handmade PRIVATE ${CMAKE_SOURCE_DIR}/src/GLAD)
target_include_directories(Handmade PRIVATE ${CMAKE_SOURCE_DIR}/src/GLM)
target_include_directories(Handmade PRIVATE ${CMAKE_SOURCE_DIR}/src/SDL)

target_link_libraries(Handmade 
${CMAKE_SOURCE_DIR}/lib/SDL/SDL2.lib 
${CMAKE_SOURCE_DIR}/lib/SDL/SDL2main.lib 
${CMAKE_SOURCE_DIR}/lib/SDL/SDL2_image.lib
${CMAKE_SOURCE_DIR}/lib/FMOD/fmod_vc.lib
${CMAKE_SOURCE_DIR}/lib/FMOD/fmodL_vc.lib
${CMAKE_SOURCE_DIR}/lib/FreeType/freetype.lib)

source_group("Header Files/Components/Core" FILES ${CMAKE_SOURCE_DIR}/src/Audio.h)
source_group("Header Files/Components/Core" FILES ${CMAKE_SOURCE_DIR}/src/Buffer.h)
source_group("Header Files/Components/Core" FILES ${CMAKE_SOURCE_DIR}/src/Material.h)
source_group("Header Files/Components/Core" FILES ${CMAKE_SOURCE_DIR}/src/Texture.h)
source_group("Header Files/Components/Core" FILES ${CMAKE_SOURCE_DIR}/src/Transform.h)
source_group("Header Files/Components/Physics" FILES ${CMAKE_SOURCE_DIR}/src/BoxCollider.h)
source_group("Header Files/Components/Physics" FILES ${CMAKE_SOURCE_DIR}/src/OBBCollider.h)
source_group("Header Files/Components/Physics" FILES ${CMAKE_SOURCE_DIR}/src/RigidBody.h)
source_group("Header Files/Components/Physics" FILES ${CMAKE_SOURCE_DIR}/src/SphereCollider.h)
source_group("Header Files/Core" FILES ${CMAKE_SOURCE_DIR}/src/App.h)
source_group("Header Files/Core" FILES ${CMAKE_SOURCE_DIR}/src/Input.h)
source_group("Header Files/Core" FILES ${CMAKE_SOURCE_DIR}/src/Screen.h)
source_group("Header Files/Core" FILES ${CMAKE_SOURCE_DIR}/src/Shader.h)
source_group("Header Files/Core" FILES ${CMAKE_SOURCE_DIR}/src/Utility.h)
source_group("Header Files/Objects/Cameras" FILES ${CMAKE_SOURCE_DIR}/src/Camera.h)
source_group("Header Files/Objects/Cameras" FILES ${CMAKE_SOURCE_DIR}/src/FreeCamera.h)
source_group("Header Files/Objects/Cameras" FILES ${CMAKE_SOURCE_DIR}/src/OrbitCamera.h)
source_group("Header Files/Objects" FILES ${CMAKE_SOURCE_DIR}/src/Model.h)
source_group("Header Files/Objects" FILES ${CMAKE_SOURCE_DIR}/src/Object.h)
source_group("Header Files/Objects" FILES ${CMAKE_SOURCE_DIR}/src/Text.h)
source_group("Header Files/Objects" FILES ${CMAKE_SOURCE_DIR}/src/Tile.h)
source_group("Header Files/States" FILES ${CMAKE_SOURCE_DIR}/src/State.h)

source_group("Source Files/Components/Core" FILES ${CMAKE_SOURCE_DIR}/src/Audio.cpp)
source_group("Source Files/Components/Core" FILES ${CMAKE_SOURCE_DIR}/src/Buffer.cpp)
source_group("Source Files/Components/Core" FILES ${CMAKE_SOURCE_DIR}/src/Material.cpp)
source_group("Source Files/Components/Core" FILES ${CMAKE_SOURCE_DIR}/src/Texture.cpp)
source_group("Source Files/Components/Core" FILES ${CMAKE_SOURCE_DIR}/src/Transform.cpp)
source_group("Source Files/Components/Physics" FILES ${CMAKE_SOURCE_DIR}/src/BoxCollider.cpp)
source_group("Source Files/Components/Physics" FILES ${CMAKE_SOURCE_DIR}/src/OBBCollider.cpp)
source_group("Source Files/Components/Physics" FILES ${CMAKE_SOURCE_DIR}/src/RigidBody.cpp)
source_group("Source Files/Components/Physics" FILES ${CMAKE_SOURCE_DIR}/src/SphereCollider.cpp)
source_group("Source Files/Core" FILES ${CMAKE_SOURCE_DIR}/src/App.cpp)
source_group("Source Files/Core" FILES ${CMAKE_SOURCE_DIR}/src/Input.cpp)
source_group("Source Files/Core" FILES ${CMAKE_SOURCE_DIR}/src/Main.cpp)
source_group("Source Files/Core" FILES ${CMAKE_SOURCE_DIR}/src/Screen.cpp)
source_group("Source Files/Core" FILES ${CMAKE_SOURCE_DIR}/src/Shader.cpp)
source_group("Source Files/Core" FILES ${CMAKE_SOURCE_DIR}/src/Utility.cpp)
source_group("Source Files/GLAD" FILES ${CMAKE_SOURCE_DIR}/src/GLAD/gl.c)
source_group("Source Files/Objects/Cameras" FILES ${CMAKE_SOURCE_DIR}/src/Camera.cpp)
source_group("Source Files/Objects/Cameras" FILES ${CMAKE_SOURCE_DIR}/src/FreeCamera.cpp)
source_group("Source Files/Objects/Cameras" FILES ${CMAKE_SOURCE_DIR}/src/OrbitCamera.cpp)
source_group("Source Files/Objects" FILES ${CMAKE_SOURCE_DIR}/src/Model.cpp)
source_group("Source Files/Objects" FILES ${CMAKE_SOURCE_DIR}/src/Object.cpp)
source_group("Source Files/Objects" FILES ${CMAKE_SOURCE_DIR}/src/Text.cpp)
source_group("Source Files/Objects" FILES ${CMAKE_SOURCE_DIR}/src/Tile.cpp)
source_group("Source Files/States" FILES ${CMAKE_SOURCE_DIR}/src/Design.cpp)

source_group("Shaders" FILES ${CMAKE_SOURCE_DIR}/Shaders/Main.frag)
source_group("Shaders" FILES ${CMAKE_SOURCE_DIR}/Shaders/Main.vert)

add_custom_command(TARGET Handmade POST_BUILD COMMAND ${CMAKE_COMMAND} -E copy_directory
${CMAKE_SOURCE_DIR}/bin/FMOD 
$<TARGET_FILE_DIR:Handmade>)

add_custom_command(TARGET Handmade POST_BUILD COMMAND ${CMAKE_COMMAND} -E copy_directory
${CMAKE_SOURCE_DIR}/bin/FreeType 
$<TARGET_FILE_DIR:Handmade>)

add_custom_command(TARGET Handmade POST_BUILD COMMAND ${CMAKE_COMMAND} -E copy_directory
${CMAKE_SOURCE_DIR}/bin/SDL 
$<TARGET_FILE_DIR:Handmade>)

add_custom_command(TARGET Handmade POST_BUILD COMMAND ${CMAKE_COMMAND} -E copy_directory
${CMAKE_SOURCE_DIR}/Assets
$<TARGET_FILE_DIR:Handmade>/Assets)

add_custom_command(TARGET Handmade POST_BUILD COMMAND ${CMAKE_COMMAND} -E copy_directory
${CMAKE_SOURCE_DIR}/Shaders
$<TARGET_FILE_DIR:Handmade>/Shaders)

add_custom_command(TARGET Handmade POST_BUILD COMMAND ${CMAKE_COMMAND} -E copy_directory
${CMAKE_SOURCE_DIR}/Assets 
${CMAKE_BINARY_DIR}/Assets)

add_custom_command(TARGET Handmade POST_BUILD COMMAND ${CMAKE_COMMAND} -E copy_directory
${CMAKE_SOURCE_DIR}/Shaders 
${CMAKE_BINARY_DIR}/Shaders)