cmake_minimum_required(VERSION 2.8.4)

project(FREESPOT_PLAN NONE)

include(../cmake/UseLATEX.cmake)

file(GLOB_RECURSE CHAPTER_FILES RELATIVE ${CMAKE_SOURCE_DIR} chapters/*.tex)
file(GLOB_RECURSE STYLES_FILES RELATIVE ${CMAKE_SOURCE_DIR} styles/*.sty)
file(GLOB_RECURSE INCLUDE_FILES RELATIVE ${CMAKE_SOURCE_DIR} include/*.pdf)

add_latex_document(main.tex 
    INPUTS ${CHAPTER_FILES} ${STYLES_FILES} ${INCLUDE_FILES}
    IMAGE_DIRS images
    BIBFILES bibliography.bib
    TARGET_NAME vaga-livre-project
    )