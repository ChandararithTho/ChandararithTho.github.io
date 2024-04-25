# 3. How to Install Windows Subsystem for Linux (Windows11)

1. TOC
{:toc}

This blog explains how to install Linux on Windows 11 for the purpose of running Deep Learning Notebook, follow Professor Brian Lovell's instruction.
•	First search “Turn windows features on or off” on laptop’s search function
•	Scroll down to buttom and make sure “Windows Subsystems for Linux” is ticked

# Install Linux on Windows with WSL
•	Open Windows Command Prompt, right-click and select "Run as administrator", enter the wsl --install command, then restart the machine.
![image](https://github.com/ChandararithTho/ChandararithTho.github.io/assets/164129658/a1665801-cb77-461e-8185-f0b0464cdfdf)
![image](https://github.com/ChandararithTho/ChandararithTho.github.io/assets/164129658/7da07f64-56a4-40e9-ba82-5e3650932159)

•	Reopen the Command Prompt, then set the WSL version 2 by typing “wsl –-set-default-version 2” then Enter
•	Update WSL to latest version, command “wsl –-update”
•	Instill WSL, command “wsl –install”
•	Set a new UNIX username and password, and reconfirm password
![image](https://github.com/ChandararithTho/ChandararithTho.github.io/assets/164129658/1370f080-74c4-4514-a618-33a1dadaef0e)
•	WSL is successfully installed and “username@machine” will then appear in green font.
![image](https://github.com/ChandararithTho/ChandararithTho.github.io/assets/164129658/ad119c99-adb1-43a7-a836-7decca05ae63)
•	Then we can access Ubuntu App by searching on Windows search function, or pin the App for easy access

#  Install Pip

•	Install Pip in WSL by commanding “sudo apt-get update && sudo apt-get install python3-pip”
•	Enter recent username and password, installation will take a few minutes
•	Memory usage confirmation question will pop up, type “Y” to confirm
![image](https://github.com/ChandararithTho/ChandararithTho.github.io/assets/164129658/e4bba848-35c7-46d2-9341-fedae9c35a8e)

# Increase Memory
•	Increase memory to avoid problems when running Deep Learning 
•	Create “.wslconfig” file on Windows, command 
“C:
cd %USERPROFILE
notepad .wslconfig
•	Copy the following text into .wslconfig.
```
# Settings apply across all Linux distros running on WSL 2
[wsl2]

# virtio9p=false  may stop crashing
#virtio9p=false

# Limits VM memory to use no more than 4 GB, this can be set as whole numbers using GB or MB
memory=8GB 

# Sets the VM to use two virtual processors
# processors=2

# Specify a custom Linux kernel to use with your installed distros. The default kernel used can be found at https://github.com/microsoft/WSL2-Linux-Kernel
# kernel=C:\\temp\\myCustomKernel

# Sets additional kernel parameters, in this case enabling older Linux base images such as Centos 6
# kernelCommandLine = vsyscall=emulate

# Sets amount of swap storage space to 8GB, default is 25% of available RAM
swap=8GB

# Sets swapfile path location, default is %USERPROFILE%\AppData\Local\Temp\swap.vhdx
# swapfile=C:\\temp\\wsl-swap.vhdx

# Disable page reporting so WSL retains all allocated memory claimed from Windows and releases none back when free
# pageReporting=false

# Turn off default connection to bind WSL 2 localhost to Windows localhost
# localhostforwarding=true

# Disables nested virtualization
# nestedVirtualization=false

# Turns on output console showing contents of dmesg when opening a WSL 2 distro for debugging
# debugConsole=true
```

•	Then we’ll need to restart WSL by commanding “wsl –shutdown” wait a moment. To check it’s actually shut down, command “wsl –running” 
•	Then command “wsl” to start WSL again

![image](https://github.com/ChandararithTho/ChandararithTho.github.io/assets/164129658/55d3e681-03de-4e3c-be30-175115ae848f)
•	Use “top” command to check memory set up




