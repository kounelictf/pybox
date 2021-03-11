# PYBOX 

The general idea of PyBox is to provide a sanboxed area, that can execute user written code, through a feature such as an Online Code IDE.
It was created to prevent the execution of Arbitary commands

![pybox](https://user-images.githubusercontent.com/62581994/110783083-f037d300-8235-11eb-94ab-5a0da08fde00.png)

## How Does IT Work

**PYBOX** is designed to run, easily and portable. It works by first setting up an Python enviornment [PyPy2](https://mail.python.org/pipermail/pypy-dev/2019-August/015797.html).
After the installation of packages and libraries are installed, Pybox sets up an confignured listening host. This is configured to the service you are using Pybox for. Upon user execution of the webbased tool or application, a request is sent from the server to Pybox, in a txt format. The code is sanitized and examined using a predefined list. If the code doesn't return any suspicious syntax, it is compiled. After compilation, the code is then sanitized again to detect any after post compilation activity. After this is done it is executed and monitored. If there is once again no suspcious activity, the print output is sent back the server and displayed to the user. If however the file does contain malicious code, it is logged, blacklisted and returns a Detection error, to the server.
