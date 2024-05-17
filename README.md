# REALTEK RTL88x2C USB Linux Driver

**Current Driver Version**: 5.12.1  
**Supported Kernels**: 2.3-6.8

## Table of Contents
1. [Introduction](#introduction)
2. [Features](#features)
3. [Requirements](#requirements)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Troubleshooting](#troubleshooting)
7. [Contributing](#contributing)
8. [License](#license)
9. [Acknowledgements](#acknowledgements)

## Introduction
This repository contains the Linux driver for the Realtek RTL88x2CU chipset, with Injection and Monitor Mode support.
It's ported to the latest kernel's and will be maintained by OpenHD.

## Features
- **Compatibility**: TBD


## Requirements
- **Linux Kernel**: >2.3
- **Build Tools**: `make`, `gcc`, and other standard build tools.

## Installation
To install the driver, follow these steps:

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/openhd/rtl88x2cu
    cd rtl88x2cu
    ```

2. **Build and Install the Driver**:
    ```bash
    make
    sudo make install
    sudo modprobe 88x2cu_ohd
    ```

## Usage
Once the driver is installed, plug in your Realtek RTL88x2CU USB wireless adapter. The system should recognize the device, and you can manage wireless connections through your network manager.

## Troubleshooting
- **Device Not Recognized**: Ensure the driver is correctly installed and loaded:
    ```bash
    sudo modprobe 88x2cu_ohd
    dmesg | grep 88x2cu_ohd
    ```
- **Build Errors**: Verify that all build dependencies are installed and that your kernel headers match your running kernel.

## Contributing
Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a Pull Request.

## License
This project is licensed under the GNU General Public License v3.0. See the [LICENSE](LICENSE) file for details.

## Acknowledgements
Special thanks to Realtek for providing the original driver source. This project builds upon their efforts to improve compatibility and performance for Linux users.
