if (${BUILD_TESTING})
  set(gtest_force_shared_crt ON CACHE BOOL "" FORCE)
  add_subdirectory(gtest)
endif (${BUILD_TESTING})

# Cereal for portable IO.
set(cereal_SOURCE_DIR "${CMAKE_CURRENT_SOURCE_DIR}/cereal" CACHE PATH "" FORCE)

# Add RapidJson
set(RapidJSON_SOURCE_DIR "${CMAKE_CURRENT_SOURCE_DIR}/rapidjson" CACHE PATH "" FORCE)

# AKAZE feature extractor.
add_subdirectory(akaze)

# Flann for fast approximate nearest neighbor searches.
add_subdirectory(flann)

# Add Optimo.
add_subdirectory(optimo)

# Add Statx.
add_subdirectory(statx)

# STLPlus for filepath tools.
add_subdirectory(stlplus3)

# Add VLFeat.
add_subdirectory(vlfeat)

# Add VisualSfM files.
add_subdirectory(visual_sfm)

# Add Rocksdb
add_subdirectory(rocksdb)