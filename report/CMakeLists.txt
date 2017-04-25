cmake_minimum_required(VERSION 2.8.4)

project(FREESPOT_PLAN NONE)

include(../cmake/UseLATEX.cmake)

add_latex_document(main.tex 
    INPUTS CMakeLists.txt
    )