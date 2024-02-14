# stm32-cmake-template



## Requirments
- `gcc-arm-linux-gnueabihf`
- `openocd`
- `cmake`
- `make`

## Building 
From `$ROOT/software/head-unit/stm32/`:
1. `cmake -B build -DCMAKE_BUILD_TYPE=Debug`
>Building in `Release` mode somehow causes issues
2. `cd build/`
3. `make`

## Uploading
From the repository root:
1. `openocd -f openocd-stlink.cfg -c "program build/head-unit.elf verify reset exit"`