# OpenCV-Installation

OpenCV (Open Source Computer Vision Library) is an open source computer vision and machine learning software library. OpenCV was built to provide a common infrastructure for computer vision applications and to accelerate the use of machine perception in the commercial products. Being a BSD-licensed product, OpenCV makes it easy for businesses to utilize and modify the code.

The library has more than 2500 optimized algorithms, which includes a comprehensive set of both classic and state-of-the-art computer vision and machine learning algorithms. These algorithms can be used to detect and recognize faces, identify objects, classify human actions in videos, track camera movements, track moving objects, extract 3D models of objects, produce 3D point clouds from stereo cameras, stitch images together to produce a high resolution image of an entire scene, find similar images from an image database, remove red eyes from images taken using flash, follow eye movements, recognize scenery and establish markers to overlay it with augmented reality, etc. OpenCV is used extensively in companies, research groups and by governmental bodies.

This Library has C++, Python, Java and MATLAB interfaces and supports Windows, Linux, Android and Mac OS. OpenCV leans mostly towards real-time vision applications and takes advantage of MMX and SSE instructions when available. A full-featured CUDA and OpenCL interfaces are being actively developed right now. There are over 500 algorithms and about 10 times as many functions that compose or support those algorithms. OpenCV is written natively in C++ and has a templated interface that works seamlessly with STL containers.

Before you can start learning OpenCV you first need to install the OpenCV library on your system. Using the Windows platform to foray into data science and computer vision is a popular choice especially among beginners. Anaconda is the first choice distribution for scientific python particularly on Windows.


- [Installing Anaconda on Windows](https://github.com/amirmohammadii/OpenCV-Installation#step-1-installing-anaconda)
- [Installing OpenCV on Windows](https://github.com/amirmohammadii/OpenCV-Installation#step-2-installing-opencv)
- [Installing Anaconda on Ununtu 18.04](https://github.com/amirmohammadii/OpenCV-Installation#step-1-installing-anaconda-1)
- [Set up Anaconda Virtual Environment on Ubuntu 18.04](https://github.com/amirmohammadii/OpenCV-Installation#set-up-anaconda-environments)
- [Uninstall Anaconda on Ubuntu 18.04](https://github.com/amirmohammadii/OpenCV-Installation#uninstalling-anaconda)
- [Installing OpenCv on Ununtu 18.04](https://github.com/amirmohammadii/OpenCV-Installation#installing-opencv)
- [Installing OpenCV on Ubuntu 18.04 without Anaconda](https://github.com/amirmohammadii/OpenCV-Installation#installing-opencv-without-anaconda)

## Install Anaconda + OpenCV on Windows

### Step 1: Installing Anaconda
Designed for data science and machine learning workflows, Anaconda is an open-source package manager, environment manager, and distribution of the Python and R programming languages. It is commonly used for large-scale data processing, scientific computing, and predictive analytics.

Offering a collection of over 1,000 data science packages, Anaconda is available in both free and paid enterprise versions. The Anaconda distribution ships with the conda command-line utility. You can learn more about Anaconda and conda by reading the official [Anaconda Documentation](https://docs.anaconda.com/).

Download the latest Anaconda graphical installer for Windows from [Anaconda website](https://www.anaconda.com/distribution/) and check for the Windows architecture on your computer. If its 64-bit then choose the 64 bit graphical installer or else choose the 32-bit installer. Choose Python 3.7 for working with Python 3. This is the preferred option as python 2.7 is reaching its End-Of-Life by 2020.

![pic1](https://user-images.githubusercontent.com/31302531/67712765-d8add080-f9d9-11e9-8807-90b3a1c17ff8.png)

Launch the graphical installer and we will be prompted to choose for which user to install.

![pic2](https://user-images.githubusercontent.com/31302531/67713010-45c16600-f9da-11e9-8593-d44e56809265.png)

Choosing “Just Me” is recommended as choosing All Users would require administrator privileges whenever we are modifying Anaconda (as will be illustrated later).

![pic2](https://user-images.githubusercontent.com/31302531/67713010-45c16600-f9da-11e9-8593-d44e56809265.png)

If we chose “Just Me” then the above dialog will be displayed with the default location being “C:\Users\<username>\Anaconda3”.

Continue to install with the default option of “Register Anaconda as the system Python 3.7” if we don’t have other versions of python or other distributions installed.

![pic4](https://user-images.githubusercontent.com/31302531/67713368-f3cd1000-f9da-11e9-8e54-1ffbadaf2c59.png)


It takes a few minutes for installation to complete. Once completed we may be prompted to optionally install VSCode as an IDE. We may skip this option if we wish to do so.

### Step 2: Installing OpenCV
Lets now come to the actual goal of installing OpenCV for python.
Launch the Anaconda prompt from the start menu:

![pic5](https://user-images.githubusercontent.com/31302531/67713621-6d64fe00-f9db-11e9-8347-6670003314fd.png)

We should see a similar prompt if we went according to instructions.

![pic6](https://user-images.githubusercontent.com/31302531/67713809-ca60b400-f9db-11e9-83d9-e36ec50de5d1.png)

if you chose “All users” while installing then you have to launch the prompt by Right-clicking and choosing “Run as Administrator” to execute with administrator privileges. **This is critical.**

If we wish to install OpenCV in a separate environment, we need to create an new environment( replace opencv with any name in the command below):

```
conda create — name opencv
activate opencv
```
(for more information about conda instructions see this [cheat sheet](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf))

To install the OpenCV we need to type the following command at the prompt:

```
conda install -c conda-forge opencv
```

However, we can alternatively choose to install through anaconda navigator graphical interface. type in “opencv” in search packages search bar. choose to install all the listed packages.

The prompt will show that it is “solving environment”. It takes quite a bit of time if you are on slower Internet connection.

![pic7](https://user-images.githubusercontent.com/31302531/67714421-1b24dc80-f9dd-11e9-92c2-e6e45bd384bd.png)

Try to use faster Internet, preferably a wired connection for uninterrupted and best results. if you are in a work or institution based Internet connection then it is likely that an HTTP timeout will occur and we need to enter the command once again and restart the procedure.
Once the environment is resolved by conda it will list the packages that will be installed, namely: *opencv, libopencv, py-opencv.*
Then enter **y** to proceed with the installation.

We can verify if the installation was successful by launching the python interpreter. opencv is referred to as cv2 in python. Type at the prompt:

```
import cv2
```

if the prompt is displayed then opencv then python has successfully imported the opencv library. But we should also verify the version of opencv so we need to type:

```
print(cv2.__version__)
```

If we want to work with a different version then while installing we can specify the version as “opencv=3.4.1" as shown below:

```
conda install -c conda-forge opencv=3.4.1
```

Similar steps can be followed to install OpenCV on anaconda for **MacOS**.

## install Anaconda + OpenCV on Ubuntu 18.04

### Step 1: Installing Anaconda
In thi part I will guide you through the steps of downloading and installing Anaconda Python Distribution on Ubuntu 18.04.
Follow the steps below to install Anaconda on Ubuntu 18.04:

1. Download the Anaconda Installation Script.

Change to the ```tmp``` directory and download the Anaconda installation script with ```wget``` or ```curl``` :
```
cd /tmp
curl -O https://repo.anaconda.com/archive/Anaconda3-5.2.0-Linux-x86_64.sh
```
The download may take some time depending on your connection speed.

2. Verify the Data Integrity of the Script.

Use the ```sha256sum``` command to verify the script checksum: 
(before that make sure that your Anacona version is 5.2 or so)
```
sha256sum Anaconda3-5.2.0-Linux-x86_64.sh
```
You should see an output like the following:
```
09f53738b0cd3bb96f5b1bac488e5528df9906be2480fe61df40e0e0d19e3d48  Anaconda3-5.2.0-Linux-x86_64.sh
```

3. Run the Anaconda Installation Script

To start the Anaconda installation process run the installation script:
```
bash Anaconda3-5.2.0-Linux-x86_64.sh
```
You should see an output like the following:

```
Welcome to Anaconda3 5.2.0

In order to continue the installation process, please review the license
agreement.
Please, press ENTER to continue
```
Press ```ENTER``` to continue and then press ```ENTER``` to scroll through the license. Once you’re done reviewing the license, you’ll be asked to approve the license terms:
```
Do you approve the license terms? [yes|no]
```
Type ```yes``` to accept the license and you’ll be prompted to choose the installation location.
```
Anaconda3 will now be installed into this location:
/home/<USERNAME>/anaconda3

    - Press ENTER to confirm the location
    - Press CTRL-C to abort the installation
    - Or specify a different location below
```

The default location is fine for most users, press ```ENTER``` to confirm the location and installation process will continue.

The installation may take some time and once it is completed, the following output will be displayed:

```
Installation finished.
Do you wish the installer to prepend the Anaconda3 install location
to PATH in your /home/<USERNAME>/.bashrc ? [yes|no]
```
If you want to use the ```conda``` command type ```yes``` press ```ENTER``` and you’ll be presented the following output:

```
Appending source /home/<USERNAME>/anaconda3/bin/activate to /home/<USERNAME>/.bashrc
A backup will be made to: /home/<USERNAME>/.bashrc-anaconda3.bak

For this change to become active, you have to open a new terminal.

Thank you for installing Anaconda3!
```
The installer will also ask you whether you would like to download and install Visual Studio Code.
```
Anaconda is partnered with Microsoft! Microsoft VSCode is a streamlined
code editor with support for development operations like debugging, task
running and version control.

To install Visual Studio Code, you will need:
    - Administrator Privileges
    - Internet connectivity

Visual Studio Code License: https://code.visualstudio.com/license

Do you wish to proceed with the installation of Microsoft VSCode? [yes|no]
```

You can find more information about [Visual Studio](https://code.visualstudio.com/). If you want to install Visual Studio Code type ```yes``` otherwise type ```no```.
To activate the Anaconda installation load the new ```PATH``` environment variable which was added by the Anaconda installer into the current shell session with the following command:
```
source ~/.bashrc
```
4. Verify the Installation

You can verify your Anaconda installation using the conda command. For example to display information about current conda install type:
```
conda info
```
You should see an output like the following:

```
    active environment : None
    user config file : /home/<USERNAME>/.condarc
populated config files :
        conda version : 4.5.4
    conda-build version : 3.10.5
        python version : 3.6.5.final.0
    base environment : /home/<USERNAME>/anaconda3  (writable)
        channel URLs : https://repo.anaconda.com/pkgs/main/linux-64
                        https://repo.anaconda.com/pkgs/main/noarch
                        https://repo.anaconda.com/pkgs/free/linux-64
                        https://repo.anaconda.com/pkgs/free/noarch
                        https://repo.anaconda.com/pkgs/r/linux-64
                        https://repo.anaconda.com/pkgs/r/noarch
                        https://repo.anaconda.com/pkgs/pro/linux-64
                        https://repo.anaconda.com/pkgs/pro/noarch
        package cache : /home/<USERNAME>/anaconda3/pkgs
                        /home/<USERNAME>/.conda/pkgs
    envs directories : /home/<USERNAME>/anaconda3/envs
                        /home/<USERNAME>/.conda/envs
            platform : linux-64
            user-agent : conda/4.5.4 requests/2.18.4 CPython/3.6.5 Linux/4.15.0-22-generic ubuntu/18.04 glibc/2.27
                UID:GID : 1000:1000
            netrc file : None
        offline mode : False
```        
5. Updating Anaconda

Updating the Anaconda is a pretty straight forward process, first update the conda tool with:
``` 
conda update conda
``` 
When prompted to confirm the update, type y to proceed.

Once conda is updated, proceed with the Anaconda update:
``` 
conda update anaconda
``` 

Same as with the previous command, when prompted, type y to proceed.

You should regularly update your Anaconda installation.

#### Set Up Anaconda Environments

You can create Anaconda environments with the ``` conda create```  command. For example, a Python 3 environment named ``` my_env```  can be created with the following command:
``` 
conda create --name my_env python=3
``` 
Activate the new environment like so:
``` 
conda activate my_env
``` 

#### Uninstalling Anaconda

If you want to uninstall Anaconda from your Ubuntu system, follow the steps below:
1. Remove the Anaconda install directory.

To remove the entire Anaconda installation directory type:
``` 
rm -rf ~/anaconda3
``` 

2. Edit the PATH environment variable.

Edit the ``` ~/.bashrc```  file and remove the Anaconda directory from the PATH environment variable:
```
# added by Anaconda3 installer
export PATH="/home/<USERNAME>/anaconda3/bin:$PATH"
```
3. Remove the hidden files.

The following rm command will remove the hidden files and folders that have been created in your user home directory:
```
rm -rf ~/.condarc ~/.conda ~/.continuum
```

### Installing OpenCV

Anaconda has a pretty lovely easy-to-use environment in which almost all the necessary Python packages are installed, and it is rapidly growing. Although OpenCV installation for anaconda has been compiled, it has different issues when it comes to integrating it with Ubuntu especially if one needs to have its complete features and especially the video support. For having all features of OpenCV, it needs to be installed from the source.

1. Installing dependencies:

Loosely speaking, installing the dependencies is the central part of OpenCV installation. The reason is OpenCV requires a lot of packages to be installed. So the system architecture must provide every single dependency that it needs. Moreover if installing extra OpenCV modules is desired, it certainly adds to the number of requirements. This section is aimed to describe what are these requirements.

   - System Update:
   
      First of all, the system packages should be updated to their latest version.
      
      ```
      sudo apt-get update
      sudo apt-get upgrade
      ```

      Building tools must be installed first. The build-essentials is a reference for any Debian package requirements. It generally     includes the gcc/g++ compilers as libraries and is necessary if any C/C++ compiler is included in the specifications. If any packages are desired to be compiled from its source, then pkg-config is required which is our case in OpenCV installation. cmake manages and executes the build process of OpenCV. cmake-curses-gui installs the ccmake which is the handy GUI for the cmake configuration process!
Build Essentials.

        ```
        sudo apt-get install build-essential 
        sudo apt-get install cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libs
        ```

   - Installing Python libraries:

      Of course, python is required for installing OpenCV. Moreover installing some great packages as Numpy and Scipy is of great   importance for any computer vision library. python-dev mainly contains the header files which are necessary to build Python extensions.
      
      ```
      sudo apt-get install python-dev python-numpy
      sudo apt-get install python-scipy
      ```

   - Installing GUI libraries:
   
     OpenCV employs the HighGUI library(“high-level graphical user interface”) to open windows, display, read and write images and videos, etc. This library(HighGUI) needs a backend to operate. There are two available backends for HighGUI. One is the Qt library which can be installed as follows:
     ```
     sudo apt-get install libgtk-3-dev
     sudo apt-get install libgtkglext1 libgtkglext1-dev
     ```
    
   - Installing image processing libraries:
   
      OpenCV is at first an image processing and manipulation library. The first ability for that is to load/save images. Moreover, it  should be able to recognize and decode different file formats like PNG, JPG, TIFF, etc. The essential packages regarding image processing can be installed as below:
      
    ```
    sudo apt-get install python3.6-dev python3-dev libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libjasper-dev libdc1394-22-dev
    ```
    
   - Installing video processing libraries:
   
      Same as images, for read/write and process videos the relevant dependencies must be installed as follows:
      
     ```
      sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev
      sudo apt-get install libxvidcore-dev libx264-dev
     ```

2. Download and Build OpenCV

download the official OpenCV release and the opencv_contrib  module using ```wget```:

```
wget -O opencv.zip https://github.com/opencv/opencv/archive/3.4.1.zip
wget -O opencv_contrib.zip https://github.com/opencv/opencv_contrib/archive/3.4.1.zip
unzip opencv.zip
unzip opencv_contrib.zip
```
- create build directory
   
```
cd ~/opencv-3.4.1/
mkdir build
cd build
```
- Now configure OpenCV using cmake
   
```
    cmake -D CMAKE_INSTALL_PREFIX=/usr/local \
      -D WITH_CUDA=OFF \
      -D WITH_QT=OFF \
      -D WITH_OPENGL=ON \
      -D OPENCV_EXTRA_MODULES_PATH=/home/<USERNAME>/soft/opencv_contrib/modules \
      -D ENABLE_FAST_MATH=ON 
      -D CUDA_FAST_MATH=ON 
      -D CUDA_NVCC_FLAGS="-D_FORCE_INLINES" \
      -D WITH_CUBLAS=ON \
      -D BUILD_OPENCV_PYTHON3=ON \
      -D PYTHON3_EXECUTABLE=/home/<USERNAME>/anaconda3/bin/python 
      -D PYTHON3_INCLUDE_PATH=/home/<USERNAME>/anaconda3/include/python3.6m 
      -D PYTHON3_LIBRARIES=/home/<USERNAME>/anaconda3/lib/python3.6/site-packages \
      -D OPENCV_ENABLE_NONFREE=ON \
      -D WITH_TBB=ON \ 
      -D WITH_V4L=ON \
      -D INSTALL_C_EXAMPLES=OFF \ 
      -D BUILD_SHARED_LIBS=ON ..
```
      
The command will take some time to execute, wait for few minutes. If the configuration is done without error, now
compiling and Installing OpenCV.

```
make -j4 #where 4 is number of core
sudo make install
 sudo ldconfig
 ```
      
At this point, Python3 bindings for OpenCV should reside in the following folder.

```
ls /usr/local/lib/python3.6/site-packages/
 ```

Let’s rename them to cv2.so:

```
cd /usr/local/lib/python3.6/site-packages/
ls
sudo mv cv2.cpython-36m-x86_64-linux-gnu.so cv2.so
```

Now, sym-link OpenCV cv2.so bindings into Anaconda-Python.

```
cd anaconda3/lib/python3.6/site-packages/
ln -s /usr/local/lib/python3.6/site-packages/cv2.so cv2.so
```

3. OpenCV Testing

```
ipython
import cv2
cv2.__version__
```

#### Installing OpenCV without Anaconda

In order to install OpenCV without using Anaconda, you can do it independently by run [this](/install_openCV) script. 
