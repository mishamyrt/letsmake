# LetsMake

Simple Android build system for ROM maintainers

## Installation

### 1. Clone repository

```sh
git clone git@github.com:mishamyrt/letsmake.git
```

### 2. Add repository folder to $PATH

```sh
cd letsmake
echo "export PATH=$PATH:$PWD" >> ~/.profile
```

### 3. Copy environment placeholder

```sh
cp .env.dist .env
```

### 4. Edit environment file
* `TARGET` — ROM/device target codename (like `aosp_X01BD-userdebug`)
* `PROJECT_FOLDER` — ROM source code folder, relative to `$HOME` 
* `AUTHOR` — name of the maintainer, used in the file name and the message when installing the kernel
* `KERNEL_NAME` — variable name speaks for itself
* `JACK_MEMORY` — amount of RAM available for JACK compiler (like `8g`)

### 5. Run

3 commands are currently available:

* `letsmake system` — builds the entire system
* `letsmake kernel` — builds only the core and packs it into the firmware archive.
* `letsmake sync` — updates source code from repositories.