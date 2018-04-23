# CMake Tutorial

For the library:
```bash
cd library
mkdir build install
cd build
cmake .. -DCMAKE_INSTALL_PREFIX=/home/sdh/Downloads/cmake-tutorial/library/install -DCMAKE_INSTALL_LIBDIR=lib
```

For the app:
```bash
cd app
mkdir build install
cd build
cmake .. -DCMAKE_INSTALL_PREFIX=/home/sdh/Downloads/cmake-tutorial/app/install
```
