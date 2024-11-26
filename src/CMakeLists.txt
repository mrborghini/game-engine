# Add the subdirectory containing the blackjack library source files
add_subdirectory(game-engine-lib)

# Specify the executable target for the main application
add_executable(game-engine
    main.c
)

# Include directories for blackjack executable
# This ensures that the blackjack executable has access to the library's headers.
target_include_directories(game-engine PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/game-engine-lib    # Includes blackjacklib's headers
)

# Link the blackjack library to the executable
target_link_libraries(game-engine PRIVATE game_enginelib)
