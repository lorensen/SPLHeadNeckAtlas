cmake_minimum_required(VERSION 2.8)
 
project(SPLHeadNeckAtlas)

configure_file(${SPLHeadNeckAtlas_SOURCE_DIR}/SPLHeadNeckAtlas.config.in  ${SPLHeadNeckAtlas_BINARY_DIR}/SPLHeadNeckAtlas.config @ONLY)

set(ATLAS_NAME SPLHeadNeckAtlas)
set(ATLAS_VOLUME_NAME Osirix-Manix-255-res)
set(ATLAS_VOLUME ${SPLHeadNeckAtlas_SOURCE_DIR}/Atlas/Osirix-Manix-255-res.nrrd)
set(ATLAS_LABELS_NAME HN-Atlas-labels)
set(ATLAS_LABELS ${SPLHeadNeckAtlas_SOURCE_DIR}/Atlas/HN-Atlas-labels.nrrd )
set(ATLAS_COLOR_TABLE_NAME HeadAndNeckAtlas-training-colors)
set(ATLAS_COLOR_TABLE ${SPLHeadNeckAtlas_SOURCE_DIR}/Atlas/HeadAndNeckAtlas-training-colors.txt.ctbl)
set(MRML_FILENAME ${SPLHeadNeckAtlas_SOURCE_DIR}/Atlas/${ATLAS_NAME}.mrml.in)

configure_file(${SPLHeadNeckAtlas_SOURCE_DIR}/Atlas/SPLHeadNeckAtlas.mrml.in  ${SPLHeadNeckAtlas_BINARY_DIR}/SPLHeadNeckAtlas.mrml @ONLY)
