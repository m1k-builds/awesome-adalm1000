# Alice
(Python, Tk/Tkinter)

# Guide to installation

On Windows, feel free to follow the official guide instead which involves less hassle and just provides an exe installer: https://wiki.analog.com/university/tools/m1k/alice/desk-top-users-guide

#### Recommended install path for Alice on your machine(without fiddling with python versions): 
(only supported on x86_64 Windows, MacOS, Linux)

<details>

<summary>Explanation: Why we are doing it this way</summary>

The official guide recommends using the (older and less maintained) conda package.

The conda package for libsmu/pysmu(as of January 2026) only supports and only runs on older python versions. We are taking it further by using Pixi by [Prefix.dev](prefix.dev) to make everyone's life easier. 

This is far from ideal but still the easiest way to run PySMU programs. @aditya-rao-iit-m's ADALM1000 [PySMU starter repo](https://github.com/aditya-rao-iit-m/adalm1000/tree/main/linux) does the same thing for linux and the difference is night and day, since you don't need to fiddle with python installations or compile libsmu from scratch.  

</details>

0. Setup Step/Small sidequest: Set up Pixi, following instructions from https://pixi.prefix.dev/latest/installation/
    - Ensure the command `pixi` works. Restart your terminal or PC if not. 
    - On Windows, also install libsmu from the official download. [Quick link for libsmu-1.0.4-setup-x64.exe](https://github.com/analogdevicesinc/libsmu/releases/download/v1.0.4/libsmu-1.0.4-setup-x64.exe)
1. Get @sounddrill31's fork with some niceties like Pixi support
    ```bash
    git clone https://github.com/sounddrill31/alice-m1k alice
    ```
2. Enter the directory
    ```bash
    cd alice
    ```
3. Let Pixi set up dependencies
    ```bash
    pixi install
    ```
4. Optional step for Linux only(for Windows and MacOS, skip to next)
    ```bash
    pixi run udev-setup
    ```
5. Start Alice Desktop through Pixi
    ```bash
    pixi run start
    ```
