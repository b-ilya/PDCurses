cmake_minimum_required(VERSION 3.10)

project(PDCursesWin)

add_library(PDCursesWin STATIC)

file(GLOB pdcurses_src "pdcurses/*.c")
file(GLOB wincon_src "wincon/*.c")

target_sources(PDCursesWin PRIVATE ${pdcurses_src})
target_sources(PDCursesWin PRIVATE ${wincon_src})

target_include_directories(PDCursesWin
        PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}
)