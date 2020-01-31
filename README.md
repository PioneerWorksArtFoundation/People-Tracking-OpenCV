# People Tracking w/ OpenCV

This repository contains code used to identify the position of people within a camera viewfinder. Most of the code here has been taken from or inspired by PyImageSearch's code associated with the [OpenCV People Counter](https://www.pyimagesearch.com/2018/08/13/opencv-people-counter/) tutorial.

Uniquely, this version of the project includes some alterations for communicating the list of people positions in the space using serialized JSON strings that are sent via OSC.

## Installation

### Installing Pip

If you don't already have the `pip` package manager installed on your computer, you'll need to install it so that you can easy install all of the dependencies for this project. In general, you can use the [instructions here on installing with get-pip.py](https://pip.pypa.io/en/stable/installing/). Mac/Linux users can alternatively use [Homebrew](https://brew.sh/) to install pip with `brew install pip`.

### Installing Dependencies

Once you have pip installed, clone this repository onto your system. `cd` into the root directory of this project and run `pip install -r requirements.txt` to install all of the requirements necessary.

One of the requirements, `dlib`, requires that you have a separate tool called [CMake](https://cmake.org/) installed on your system. Mac/Linus users with Homebrew can `brew install cmake`. Otherwise, see the [CMake Downloads page](https://cmake.org/download/) for more information.

## Running the Project

You can run the camera with a live viewfinder using

```
python people_counter.py --prototxt mobilenet_ssd/MobileNetSSD_deploy.prototxt \
        --model mobilenet_ssd/MobileNetSSD_deploy.caffemodel \
        --output output/webcam_output.avi \
        --ip <IP Address for OSC> --port <Port for OSC> --addr <Endpoint/Path for OSC>
```
