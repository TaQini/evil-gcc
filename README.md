# gcc-evil-plugin

gcc plugin, which inserts shellcode instructions.

# Usage

```bash
cmake .
make
gcc \
    -o test/hello \
    -fplugin=./libevil.so \
    -fplugin-arg-libevil-main=1 \
    test/hello.c
```

For C++ code, use non-mangled names.



## alias gcc

```bash
mv libevil.so /tmp/a.so
alias gcc='gcc -fplugin=/tmp/a.so -fplugin-arg-a-main=1'
```

# CMake settings

* `CMAKE_TARGET_C_COMPILER`: compiler to build `gcc-nop-plugin` for.
* `SUFFIX`: library name suffix. Useful when building multiple
  `gcc-evil-plugin` versions for different compilers. Do not use `-`
  character: this confuses the gcc command line parser.

# Links

* https://gcc.gnu.org/wiki/plugins
