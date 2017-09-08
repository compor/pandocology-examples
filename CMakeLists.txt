# cmake file

cmake_minimum_required(VERSION 2.8)

project(pandocology-example NONE)


list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake/cmake-pandocology")

include(pandocology)

#

add_subdirectory(src)

add_document(
  TARGET todo3
  OUTPUT_FILE TODO3.html
  SOURCES src/TODO2.md)

add_document(
  TARGET todo4
  OUTPUT_FILE TODO4.html
  SOURCES TODO.md)

# this should give a warning on configure
# this should cause a circular dep error on build
#add_document(
  #TODO.html
  #SOURCES TODO.md)

# this should cause an error
#add_document(
  #src/TODO2.html
  #SOURCES src/TODO2.md)

# this should cause an error
#add_document(
  #TARGET TODO5.html
  #OUTPUT_FILE TODO5.html
  #SOURCES TODO.md)

