# VoiKaPi Microexpression
## Mission Statement
Hello everyone! Welcome to our exciting new project focused on microexpression detection using the Raspberry Pi. Our goal is to create an affordable and portable device that can accurately detect microexpressions in real-time, without relying on an internet connection. This project has the potential to revolutionize fields such as psychology, criminology, and marketing.

## Appeal for Contributions
To make this project a reality, we need your help! We are currently seeking financial and programming contributions from anyone interested in supporting our cause. Your support will assist in purchasing the necessary hardware and software, as well as funding ongoing research and development.

If you are interested in contributing, please visit the project's about section and click the link. Every little bit helps, and we appreciate any support you can give. Thank you!

## Project Overview
Our project aims to create an affordable and portable microexpression detection device using a Raspberry Pi and a machine learning model. The device will be designed to run offline, helping individuals with social anxiety and autism improve their social interactions. We strive to provide a user-friendly and customizable solution that is accessible to anyone with basic programming knowledge.

### Hardware
To build the microexpression detection device, the following hardware components are required:

- Raspberry Pi 4 Model B (4GB RAM) - $120
- CanaKit Raspberry Pi 4 Power Supply - $9
- Samsung 64GB MicroSDXC EVO Select Memory Card - $11
- Raspberry Pi 4 Case with Fan and Heatsinks - $17
- Logitech C920x Pro HD Webcam - $70
- OpenCV AI Kit (OAK-D) - $249

#### For the GPU, we recommend the following options:

- EVGA GeForce GT 710 2GB GDDR5 Low Profile Graphics Card - $70

Total cost with EVGA GT 710 GPU: $476

- Alternative option: ASUS NVIDIA GT 710 2GB GDDR5 Graphics Card - $65

Total cost with ASUS GT 710 GPU: $471

> Please note that prices may vary based on location and availability.

#### GPU enclosure and related power supply
We are still in the process of selecting an external GPU enclosure and related power supply. @apple-fritter finds [Jeff Geerling](https://github.com/geerlingguy)'s project [pi4gpu](https://github.com/geerlingguy/pi4gpu) to be very impressive. Please go visit his project and give him support, as well!

### Build Instructions
Follow these step-by-step instructions to assemble and configure the microexpression detection device:

#### Assemble hardware
- Connect the Raspberry Pi to a monitor, keyboard, and mouse.
- Attach the GPU to the Raspberry Pi using a compatible interface such as USB or Thunderbolt.
- Connect the camera to the Raspberry Pi.

#### Install Ubuntu Mate on Raspberry Pi
Download the Ubuntu Mate operating system image from the official website.
- Write the image to a MicroSD card using a tool like BalenaEtcher.
- Insert the MicroSD card into the Raspberry Pi and power it on.
- Follow the prompts to complete the installation.
- Install required software packages

Open a terminal window on the Raspberry Pi and run the following commands:
```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install python3-opencv python3-numpy python3-scipy python3-matplotlib
```
These commands will install `OpenCV`, `NumPy`, `SciPy`, and `Matplotlib` on the Raspberry Pi.

#### Configure GPU for use with Raspberry Pi

Follow the manufacturer's instructions to install any necessary drivers or software for the GPU.

Open a terminal window on the Raspberry Pi and run the following commands to install the necessary software for using the GPU with the Raspberry Pi:

```bash
sudo apt-get install libdrm-dev libgbm-dev libx11-dev mesa-utils
sudo apt-get install mesa-opencl-icd ocl-icd-opencl-dev
```
Reboot the Raspberry Pi.
#### Install OpenFace library

Open a terminal window on the Raspberry Pi and run the following commands:
```bash
sudo apt-get install build-essential cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
sudo apt-get install python3-dev python3-numpy libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libdc1394-22-dev
cd ~/
git clone https://github.com/TadasBaltrusaitis/OpenFace.git
cd OpenFace
mkdir build
cd build
cmake -D CMAKE_BUILD_TYPE=RELEASE ..
make
```
This will download and install the `OpenFace` library on the Raspberry Pi.

## Test the microexpression detection system

#### Write a Python script
- Capture video from the camera and analyze it for microexpressions using OpenCV and the pre-trained models provided by the OpenFace library.
- Run the script and verify that the microexpression detection system is working correctly.

## Use the system to detect microexpressions offline

Once the microexpression detection system is working correctly, you can use it to detect microexpressions offline without an internet connection.

For example, you could use the system to analyze video recordings of social interactions and identify patterns in facial expressions.

Please keep in mind that this is a general guide, and you may need to modify the steps based on your specific hardware and software configuration. However, following these steps should give you a good starting point for building your own offline microexpression detection device using the OpenFace library.

## Disclaimer
Please note the following disclaimer regarding the software used in this project:

**This software is provided "as is" and without warranty of any kind**, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and noninfringement. In no event shall the authors or copyright holders be liable for any claim, damages, or other liability, whether in an action of contract, tort, or otherwise, arising from, out of, or in connection with the software or the use or other dealings in the software.

The authors do not endorse or support any harmful or malicious activities that may be carried out with the software. **It is the user's responsibility to ensure that their use of the software complies with all applicable laws and regulations**.

## License
These files are released under the [MIT License](LICENSE).
