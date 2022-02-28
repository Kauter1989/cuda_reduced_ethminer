# ethminer

This is a reduced version of ethminer. It supports only simulation mode and mines only with CUDA devices. 

Your task is to implement the main part of the mining kernel (so called "memory hard" loop). See the "TODO" comment in ./libethash-cuda/dagger_shuffled.cuh

## Build environment

Windows 10, VS 2019

## Build dependencies

1. CUDA toolkit (11.3)
2. boost (1.75)
3. jsoncpp (1.9.4)
4. CLI11 (1.9.0)

The simpliest way to install boost, jsoncpp and CLI11 is to use vcpkg (see https://vcpkg.io/en/getting-started.html)

## Usage

`ethminer --benchmark <block_number> <additional_options>`

1. Select the block number so that the DAG fits devices global memory size.
2. Find out kernel execution control options: `ethminer.exe --help-ext cu`
