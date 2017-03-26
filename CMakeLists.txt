PROJECT(FreeRtos)
CMAKE_MINIMUM_REQUIRED(VERSION 3.5) #as I just test with this version

SET(CMAKE_C_FLAGS " -fno-common -fno-builtin -ffreestanding  -nostdinc ")
set(CMAKE_EXE_LINKER_FLAGS " -T ${CMAKE_SOURCE_DIR}/my.lds -static ")
SET(CMAKE_C_LINK_EXECUTABLE "/usr/bin/ld <CMAKE_C_LINK_FLAGS> <LINK_FLAGS> <OBJECTS>  -o <TARGET>")
AUX_SOURCE_DIRECTORY(. MYSRC)
ADD_EXECUTABLE(my ${MYSRC})
