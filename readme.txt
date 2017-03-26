gcc -c my.c
ld -T my.lds -o my my.o

or

mkdir build

cd build

cmake -DCMAKE_TOOLCHAIN_FILE=../toolchain.cmake ..

<modify CMakeFiles/my.dir/link.txt ,add -T /workspace/repos/github/pine64/cmake_test/my.lds>

make
