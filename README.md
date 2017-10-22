# Learning Computer Vision with OpenCV

## Introduction

The main purpose of this work is to translate the exercises proposed in the class _Sistemas de Percepción_ of _Universidad de Málaga_ from `MATLAB` to `OpenCV Python`. `MATLAB` is a great tool for computer vision, maybe the standard tool in the industry, but the fact that it's propietary software makes it too inaccesible to the broad learning public. Fortunately, the Open Source Community has done an outstanding work to overcome this issue developing and releasing a set of great tools that make computer vision avaible to everyone who is interested.

`OpenCV` is the main open source tool for computer vision with, according to its website, a community of 47 thousand people and a estimated number of downloads exceeding 14 million. It covers a great amount of computer vision algorithms, with most `MATLAB` functions having its equivalents in `OpenCV`.

I have chosen `Python` as the core programming language because of its readabilty, its resemblance to `MATLAB` and its increasing usage for all aspects surrounding computer vision. This way, we could easily use our code along with any other `Python` library as `TensorFlow` and `Sci-kit Learn` for machinge learning, `Django` and `Flask` for web  applications developing, `Seaborn` for advanced data visualization and `ROS` for robotics programming and simulation, among many others.

The project is presented in `Jupyter Notebooks`, each notebook covering a set of exercised related to a certain broad topic in computer vision. `Jupyter Notebooks` allow the user to interact easily with the code, evaluating the consequences of one or a set of lines of code, showing numerical outputs, printings and even images. One can quickly know the results of applying a certain algorithm to an image. 

The original set of exercises were originally designed by the _Ingenería de Sistemas y Automática (ISA)_ of _Universidad de Málaga_ for the class _Sistemas de Percepción_. The translated excercises are presented as more similar to the original ones as possible, just changing the `MATLAB` commands referenced and some consequences resulting of not using them. They are accompanied with explanations on how to use the functions needed to solve the problem, as well as with commentaries to the results obtained. Sometimes, even some computer vision theory concepts are presented.

The work is not completely finished: sometimes because `OpenCV` does not hold equivalents for some `MATLAB` functions, but mainly because of my inexperience with the tools. I hope it will be completed some time soon and, why note, even expanded.

$$
$$

_Alejandro Solano Rueda, 2017_


## Set the environment

The best practice to work with `Python` nowadays is to use `Anaconda`. Anaconda is a platform to manage Python packages easily, installing and uninstalling libraries as we need to. It is supported for Linux, MacOS and Windows.

The first step would be to [download](http://www.anaconda.com/download/) and install Anaconda. Once the installation is completed, go to the command line and type:
```
conda create -n opencv python=3.6
```

You have just created a so called _conda environment_, which we will name `opencv`. A conda environment could be seen as a virtual machine for `Python` in which you install and uninstall packages without affecting other environments. In this case, our environment is set to use the version 3.6 of `Python`.

Next step is to get into that environment. 
```
source activate opencv
```

If you are using a Windows operative system, do instead:
```
activate opencv
```

Once you are working within your environment, it's time to download the packages that will be used throught these project.
```
conda install numpy matplotlib jupyter notebooks
```

`Numpy` is a computational package for `Python` which will provide us with a large set of mathematical operations equivalent to those of `MATLAB`. The fact that is built in `C` makes computations efficient and fast. The main data structure of `Numpy` is the numpy-array. This structure guarantees efficienty when working with vectors and matrices. The images in `OpenCV Python` are read as numpy arrays.

The `Matplotlib` library will cover our plotting necessities, including the visualization of images. Once again, it resemblace to `MATLAB` is notorious.

Finally, install the OpenCV package in your environment.
```
conda install -c menpo opencv3
```

Now, just go to the 'notebooks' folder and type:
```
jupyter-notebook
```

A tab will open in your default web browser.
