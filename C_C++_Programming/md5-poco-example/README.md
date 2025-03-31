# Prerequisites
sudo apt update \
sudo apt install python3-pip \
pip3 install --user conan
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc \
source ~/.bashrc \
conan --version

sudo apt install cmake -y

conan profile detect

# Build and Run on Linux Ubuntu
rm -rf build \
mkdir build && cd build

## Conan install with new generators
conan install .. --build=missing

## Configure with CMake toolchain file provided by Conan
cmake .. -DCMAKE_TOOLCHAIN_FILE=conan_toolchain.cmake -DCMAKE_BUILD_TYPE=Release

## Build the application
cmake --build .

# Run your application
./md5_poco_example
