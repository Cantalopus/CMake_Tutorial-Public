## From Bash, run:

```Bash
rm -rf build
cd ~/notes/CMake_Tutorial/00_Before_You_Begin/Step0
cmake -S . -B build
cmake --build build
./build/hello
```

[Click Here](../Step0/CMakeLists.txt#cd-~/notes/CMake_Tutorial/00_Before_You_Begin/Step0) to see the Listfile(CMakeLists.txt)
  
## Also try:

```Bash
cd ~/notes/CMake_Tutorial/00_Before_You_Begin/Step0
cmake -G "Ninja Multi-Config" -S . -B build --fresh
cmake --build build --config Debug
./build/Debug/hello
```

### Notice 3 things in the previous 4 commands:  
 
- The `-G` flag, to select a generator(*Ninja Multi-Config*) 
- The `--fresh` command(instead of using `rm rf build`)  
- and, selecting the `Debug` configuration using the command `--config` followed by the configuration, here we are build with the `Debug` configuration. 