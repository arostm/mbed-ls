## Description
mbed-lstools is module used to detect and list mbed-enabled devices connected to host computer.
Currently lmtools support listed below OSs:
* Windows 7.
* Ubuntu.

mbed-ls is Python module used to detect and list mbed-enabled devices connected to host computer. package will support Windows 7, Ubuntu and MacOS. It will be delivered as redistributable Python module (package) and command line tool.
Currently mbed-ls module is under development but already decoupled mbed-ls functionality is delivered to mbed SDK's test suite.

You will be able for example to use this tool from command line! (See below)
### mbedls command line tool
After installing mbed-ls package on your system will be deployed importable ```mbed_lstools``` Python package and ```mbedls``` command line tool:
```
$ mbedls
+---------------------+-------------------+-------------------+--------------------------------+
|platform_name        |mount_point        |serial_port        |target_id                       |
+---------------------+-------------------+-------------------+--------------------------------+
|KL25Z                |I:                 |COM89              |02000203240881BBD9F47C43        |
|NUCLEO_F302R8        |E:                 |COM34              |07050200623B61125D5EF72A        |
+---------------------+-------------------+-------------------+--------------------------------+
```

```mbedls``` commad will allow you to list all connected mbed-enabled devices and correctly assoricate mbed-enabled board mount point (disk) and serial port. Additionally TargetID information will be provided for your reference. Because we are all automation fanatics ```mbedls``` command will also output mbed-enabled auto-detection data in JSON format.
If you want to use ```mbedls``` in your toolchain, continuous integration or automation script and do not neceserly want to use Python module ```mbed_lstools``` this solution is for you.

### Rationale
When connecting more than one mbed-enabled device to host computer it takes time to check platform's binds:
* Mounted disk.
* Virtual serial port.
* Mbed's TargetId and generic platform name.

# Installation from Python sources 
Prerequisites: you need to have Python 2.7.x installed on your system.

To install mbed-ls module clone mbed-ls repository:
```
$ git clone <link-to-mbed-ls-repo>
```
and move to mbed-ls repository directory:
```
$ cd mbed-ls
```
Now you are ready to install mbed-ls. 


# Installation from PyPI (Python Package Index)
In the near furure mbed-ls module can be redistributed via PyPI. We recommend you use ```pip``` application. It is available here: https://pip.pypa.io/en/latest/installing.html#install-pip
```
Note: Python 2.7.9 and later (on the python2 series), and Python 3.4 and later include pip by default [1], so you may have pip already.
```
