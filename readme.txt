gcc -c my.c
ld -T my.lds -o my my.o

or

mkdir build

cd build

cmake -DCMAKE_TOOLCHAIN_FILE=../toolchain.cmake ..

make
