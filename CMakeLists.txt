cmake_minimum_required(VERSION 2.8)
 
get_filename_component(PROG ${CMAKE_SOURCE_DIR} NAME)
project(${PROG})

set(ATLAS_NAME ${PROJECT_NAME})

set(ATLAS_VOLUME_NAME Osirix-Manix-255-res)
set(ATLAS_VOLUME ${CMAKE_SOURCE_DIR}/Atlas/Osirix-Manix-255-res.nrrd)

set(ATLAS_LABELS_NAME HN-Atlas-labels)
set(ATLAS_LABELS ${CMAKE_SOURCE_DIR}/Atlas/HN-Atlas-labels.nrrd)

set(ATLAS_COLOR_TABLE_NAME HeadAndNeckAtlas-training-colors)
set(ATLAS_COLOR_TABLE ${CMAKE_SOURCE_DIR}/Atlas/HeadAndNeckAtlas-training-colors.txt.ctbl)

set(MRML_FILENAME ${CMAKE_SOURCE_DIR}/Atlas/${ATLAS_NAME}.mrml.in)

configure_file(${CMAKE_SOURCE_DIR}/${ATLAS_NAME}.config.in  ${CMAKE_BINARY_DIR}/${ATLAS_NAME}.config @ONLY)

configure_file(${CMAKE_SOURCE_DIR}/Atlas/${ATLAS_NAME}.mrml.in  ${CMAKE_BINARY_DIR}/${ATLAS_NAME}.mrml @ONLY)
cmake_minimum_required(VERSION 2.8)
