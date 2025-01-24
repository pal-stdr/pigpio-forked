- You can find the original README.md here [README.md](README.md).

# How to Build

## For installing in root fs (i.e. `/usr/local/`)

```sh

# Installing in a custom path
sudo make install

# Clean the current lib root
make custom-clean INSTALLATION_DIR=$PWD/pigpio-installation
```

## For installing in custom path...

```sh

# Installing in a custom path
make custom-install INSTALLATION_DIR=$PWD/pigpio-installation

# Clean the current lib root
make custom-clean INSTALLATION_DIR=$PWD/pigpio-installation
```

## If you are using arch specific compiler like `aarch64-linux-gnu-gcc` to build this lib then use `CROSS_PREFIX=aarch64-linux-gnu-`

```sh
# Installing in a custom path
make custom-install INSTALLATION_DIR=$PWD/pigpio-installation CROSS_PREFIX=aarch64-linux-gnu-

# Clean the current lib root
make custom-clean INSTALLATION_DIR=$PWD/pigpio-installation
```

# After custom installation

```sh
pigpio-installation/
├── bin
│   ├── pig2vcd
│   ├── pigpiod
│   ├── pigs
│   ├── x_pigpio
│   ├── x_pigpiod_if
│   └── x_pigpiod_if2
├── include
│   ├── pigpiod_if2.h
│   ├── pigpiod_if.h
│   └── pigpio.h
└── lib
    ├── libpigpiod_if2.so -> libpigpiod_if2.so.1
    ├── libpigpiod_if2.so.1
    ├── libpigpiod_if.so -> libpigpiod_if.so.1
    ├── libpigpiod_if.so.1
    ├── libpigpio.so -> libpigpio.so.1
    └── libpigpio.so.1
```