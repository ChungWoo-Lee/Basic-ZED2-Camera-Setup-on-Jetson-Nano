# ZED2 Camera Basic Setup on Jetson Nano

This repository provides basic code for setting up and visualizing the ZED2 camera on Jetson Nano. Follow the steps below to configure your environment and run the code successfully.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Troubleshooting](#troubleshooting)
- [References](#references)

---

## Prerequisites

Before running the ZED2 camera on Jetson Nano, ensure you have the following:
- Jetson Nano Developer Kit
- ZED2 Camera
- JetPack installed on Jetson Nano (tested with JetPack 4.6)
- ZED SDK installed (latest version)
- Python 3.7 or above

## Setup Instructions

1. **Install ZED SDK:**
   - Visit the official [ZED SDK download page](https://www.stereolabs.com/developers/release/) and download the appropriate version for Jetson Nano.
   - After downloading, install the SDK by running:
     ```bash
     chmod +x ZED_SDK_UbuntuXX_JPXX_vX.X.X.run
     ./ZED_SDK_UbuntuXX_JPXX_vX.X.X.run
     ```
     Replace `XX` and `X.X.X` with the correct version numbers for your Jetson Nano environment.
   - Follow the on-screen instructions to complete the installation.

2. **Install Python Dependencies:**
   - Ensure the following Python packages are installed:
     ```bash
     sudo apt-get install python3-pip
     pip3 install cython pyopengl numpy opencv-python
     ```
   - Additionally, install the ZED Python API:
     ```bash
     pip3 install pyzed
     ```

3. **Connect ZED2 Camera:**
   - Plug in the ZED2 camera via USB 3.0 into your Jetson Nano.
   - Ensure that the camera is properly detected by running:
     ```bash
     lsusb
     ```

## Usage

1. **Running the Example Code:**
   - Clone this repository to your Jetson Nano:
     ```bash
     git clone https://github.com/your-username/zed2-jetson-nano-basic.git
     cd zed2-jetson-nano-basic
     ```
   - Run the visualization script:
     ```bash
     python3 zed2_visualization.py
     ```

2. **Expected Output:**
   - The script will launch a window that shows the live camera feed from the ZED2 camera.
  
## Troubleshooting

- **ZED SDK not installed correctly:**  
  If you encounter any issues during installation, ensure that you are using the correct version of the ZED SDK for your JetPack version.

- **Camera not detected:**  
  If the ZED2 camera is not recognized, ensure that it is connected via USB 3.0 and run `lsusb` to verify the connection.

- **Performance issues:**  
  To improve performance on Jetson Nano, consider lowering the camera resolution or adjusting the depth mode in the SDK settings.

## References

- [Stereolabs ZED SDK Documentation](https://www.stereolabs.com/docs/)
- [Jetson Nano Official Setup](https://developer.nvidia.com/embedded/jetson-nano-developer-kit)
- [Tutorial by Dohyeon (Korean)](https://dohyeon.tistory.com/19)
