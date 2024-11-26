# Define the blackjack library
add_library(game_enginelib
    cat.c
)

# Include directories for the blackjack library
# This makes the headers available to anyone linking against blackjack_lib.
target_include_directories(game_enginelib PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}   # Includes blackjack's headers (card.h, suit.h)
)
