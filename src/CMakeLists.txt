

add_document(
  TARGET readme1
  OUTPUT_FILE README1.html
  SOURCES README.md)

add_document(
  README2.html
  SOURCES README.md)

# this should cause an error
#add_document(
  #README.html
  #doesnotexist.html
  #SOURCES README.md)


