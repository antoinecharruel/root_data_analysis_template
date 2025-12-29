# README.md

# Download a pre-compiled binary distribution

Download the release for the desired platform and ROOT version:
https://root.cern/install/all_releases/

# Install

Place ROOT in the following directory: \third_party\root

## Build

```powershell
mkdir build
cd build
cmake -G "Visual Studio 17 2022" ..
cmake --build . --config Debug -- /m

```

## Run

Use Developer Command Prompt for VS 2022