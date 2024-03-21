# smc_cppserial_lib
This is a child project of the Samuko IMU Compute (SIC) project. This library helps communicate with the already setup IMU (`MPU9250 module`) in you PC or microcomputer-based python projects, after successful setup with the [**`sic_calibration_py_codes`**](https://github.com/samuko-things-company/sic_calibration_py_codes).

> you can use it in your microcomputer robotics project **running on linux** (e.g Raspberry Pi, PC, etc.)

A simple way to get started is simply to try out and follow the example code in the example folder


## How to Use the Library
- install the libserial-dev package
  > sudo apt-get update
  >
  > sudo apt install libserial-dev

- Ensure you have the **`sic_mpu9250_driver module`** interfaced with the **`MPU9250`** module. setup and cilibrate it using the **`sic_calibration_py_codes`**.

- Download (by clicking on the green Code button above) or clone the repo into your PC.

- A simple way to get started is simply to try out and follow the example `read_rpy.cpp` code.

- make, build and run the example code.
  > cd into the root directory
  >
  > mkdir build (i.e create a folder named build)
  >
  > enter the following command in the terminal in the root folder:
    ````
    cmake -B ./build/
    ````
    ````
    cmake --build ./build/
    ````
    ````
    ./build/read_rpy
    ````

- You can follow the pattern used in the example `read_rpy.cpp` in your own code.


## Basic Library functions and usage

- connect to sic_driver shield module
  > .connect("port_name or port_path")

- get filtered Roll, Pitch and incremental Yaw values
  > getRPY(&roll, &pitch, &yaw)

- get filtered absolute Yaw orientation readings
  > getHeading(&yaw_abs)

- get Roll, Pitch and Yaw rates value
  > getRPYrate(&roll_rate, &pitch_rate, &yaw_rate)

- get linear acceleration values ax, ay, az
  > getLinAcc(&ax, &ay, &az)