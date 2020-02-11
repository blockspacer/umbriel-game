set_directory_properties(PROPERTIES CORRADE_USE_PEDANTIC_FLAGS ON)

add_executable(UmbrielGame source/main.cpp)

set_target_properties(UmbrielGame
	PROPERTIES ${DEFAULT_PROJECT_OPTIONS}
)

target_include_directories(UmbrielGame
	PRIVATE
		${CMAKE_CURRENT_SOURCE_DIR}
	PUBLIC
		${DEFAULT_INCLUDE_DIRECTORIES}
)

target_link_libraries(UmbrielGame
	PRIVATE
		Json ImGUI

		Corrade::Containers
		Corrade::Utility
		Corrade::Main

		Magnum::Magnum
		Magnum::GlfwApplication
		Magnum::SceneGraph
		Magnum::Primitives
		Magnum::MeshTools
		Magnum::Shaders
		Magnum::Trade
		Magnum::GL
	PUBLIC
		${DEFAULT_LIBRARIES}
)

target_compile_definitions(UmbrielGame
	PRIVATE
	PUBLIC
		${DEFAULT_COMPILE_DEFINITIONS}
)

target_compile_options(UmbrielGame
	PRIVATE
	PUBLIC
		${DEFAULT_COMPILE_OPTIONS}
)

target_link_libraries(UmbrielGame
	PRIVATE
	PUBLIC
		${DEFAULT_LINKER_OPTIONS}
)