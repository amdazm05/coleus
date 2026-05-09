# System Requirements

- CMake (what version)
- Python (what version)
- Rust (1.95+)
- cffi (what version)
- openssl (3.5.0)
- Arm Toolchain (GCC 15.1.+)

# Evironments Tested

The following environments have been tested.
- Ubuntu 24.04

## Setting Environment

```
  python -m venv .venv
  source .venv/bin/activate
  pip3 install west

```
### Trusted Firmware M - Build Instruction
It is important to use a python venv setup passed to TF-M, to use an isolated environment.

Note: These packages are needed by Python for building.

```
  python3 -m venv .venv
  source .venv/bin/activate
  python3 -m pip install --upgrade pip
  python3 -m pip install .

```

For CMake configuration
```
  cmake -S . -B build \
    -DTFM_PLATFORM=<PLATFORM_PORT_PATH> \
    -DPython3_EXECUTABLE=$VIRTUAL_ENV/bin/python

```
## Disclaimer 
Private Developer Preview. Not for distribution.
