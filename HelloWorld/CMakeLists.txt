project(HelloWorld)
IF (MINGW) # msys
	set(CMAKE_CXX_COMPILER "/mingw64/bin/g++") # fixed CXX set /mingw64/bin/CC.exe
	set(CMAKE_EXE_LINKER_FLAGS " -static") # include libgcc_s_seh-1.dll, libstdc++-6.dll to exe file
ENDIF()
add_executable(HelloWorld "./HelloWorld.cpp")
