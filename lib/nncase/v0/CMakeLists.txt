include_directories(${SDK_ROOT}/third_party/xtl/include ${CMAKE_CURRENT_LIST_DIR}/nncase/include)

FILE(GLOB_RECURSE NNCASE_SRC
        "${CMAKE_CURRENT_LIST_DIR}/*.c"
        "${CMAKE_CURRENT_LIST_DIR}/*.cpp"
        )

ADD_LIBRARY(nncase-v0
        ${NNCASE_SRC}
        )
TARGET_COMPILE_OPTIONS(nncase-v0 PRIVATE -O2)