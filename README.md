# socat
Mirror of the socat source code with pre-built releases for Windows, Linux (x64 and x86), and MacOS (x64)

# Releases
Both x64 and x86 binaries for Linux and Windows can be downloaded from the "Releases" section of this repo. An x64 MacOS binary is available as well:
- https://github.com/3ndG4me/socat/releases

# Build Instructions

## Linux:
1. Make sure gcc, make, and openssl are installed
2. Clone or download the zip for this repo `git clone https://github.com/3ndG4me/socat.git`
3. `cd socat`
4. `./configure`
5. `make`
6. A `socat` binary will be in the root of the socat repo
7. *Optional* `make install` (will install socat into your path)

## Windows:
1. Install Cygwin with the following additional packages:
    - `gcc-g++`
    - `gcc-core`
    - `cygwin32-gcc-g++`
    - `cygwin32-gcc-core`
    - `make`
2. Using Cygwin, clone or download the zip for this repo `git clone https://github.com/3ndG4me/socat.git`
3. `cd socat`
4. `./configure`
5. `make`
6. A `socat.exe` binary will be in the root of the socat repo
7. *Optional* `make install` (will install socat into your path)

## MacOS
1. Be sure clang/gcc is installed along with make, and openssl
2. Clone or download the zip for this repo `git clone https://github.com/3ndG4me/socat.git`
3. `cd socat`
4. `./configure`
5. `make`
    - *NOTICE*: For version 1.7.3.3 the `xio-termios.c` file had a function call on line `359` that passed the parameter `speed` as the type of `speed_t`. According the interface for this function, defined in the `xio-termios.h` header file, this paramter is supposed to be an `unsigned int`. This is a strange error that only occurs with the mac version during the intial build with `make`. It is simply patched by changing the `speed_t` type of the `speed` parameter to the `unsigned int` that the interface is expecting.
6. A `socat` binary will be in the root of the socat repo
7. *Optional* `make install` (will install socat into your path)



# Notice:
I did not write this, nor do I maintain the original project. This is simply a mirror repo hosting pre-compiled release builds. All original licenses apply. All credit goes to the original creator/maintainer, please visit the link to the original maintainer below for more information on how to report bugs and about the socat project in general:
- http://www.dest-unreach.org/socat/

Also checkout the original README below for more information:
- https://github.com/3ndG4me/socat/blob/master/README
