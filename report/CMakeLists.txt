cmake_minimum_required(VERSION 2.8.4)

project(FREESPOT_PLAN NONE)

include(../cmake/UseLATEX.cmake)

file(GLOB_RECURSE CHAPTER_FILES RELATIVE ${CMAKE_SOURCE_DIR} chapters/*.tex)

add_latex_document(main.tex 
    INPUTS ${CHAPTER_FILES}
    IMAGE_DIRS images
    )