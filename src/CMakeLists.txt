cmake_minimum_required (VERSION 3.8)

aux_source_directory(. src)
add_executable (FileExchanger ${src})
set_target_properties(FileExchanger PROPERTIES DEBUG_POSTFIX "d") 
set_target_properties(FileExchanger PROPERTIES OUTPUT_NAME "FileExchanger.${FILENAME_SUFFIX}")
if (UNIX)
	TARGET_LINK_LIBRARIES(FileExchanger dl)
endif()
link_directories(${OUTDIR})

