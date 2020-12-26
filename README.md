   # ToolBox

https://github.com/ventoy/Ventoy/releases - USB multiboot solution

   ## Useful ISOs
https://ubuntu.com/download/desktop

https://ubuntu.com/download/server

https://sergeistrelec.ru/  - WinPE with live multitools

https://www.hirensbootcd.org/ - Community Edition of the famouse live CD

   
   ## Windows Scripts

https://github.com/ChrisTitusTech/win10script


   ## Installing RTL8821CE Network Controller
 
   ###### Method #1
 
   *Credits: https://medium.com/@kimiyukiyukawa/installing-rtl8821ce-network-controller-on-ubuntu-335d8ccb8a92*

   - Know what driver are you using, open terminal and write:
     `lspci | grep Network`
     
   - Go to https://github.com/tomaspinho/rtl8821ce and download the repo.
   - Unzip the file and rename the folder from *`rtl8821ce-master to rtl8821ce`* (You have to rename the file properly or the error would rise)
   - Run these on terminal
      ````
      cd Downloads/rtl8821ce/
      sudo apt install bc module-assistant build-essential dkms
      sudo m-a prepare
      sudo ./dkms-install.sh
      ````

   - Wait until it’s done and then reboot your PC.
   - On some case you might need to disable secure boot if the driver hasn’t installed yet after you follow the steps above.

   ###### Method #2
   
   *Credits: https://github.com/tomaspinho/rtl8821ce* (original author of the driver)
   
  ## DKMS

This driver can be installed using DKMS. This is a system which will automatically recompile and install a kernel module when a new kernel gets installed or updated. To make use of DKMS, install the dkms package.

 ## Installation of Driver

Make sure you have a proper build environment and dkms installed.

 ## Ubuntu & Debian

The following steps are required prior to building the driver on Ubuntu/Debian:

``
sudo apt install bc module-assistant build-essential dkms
sudo m-a prepare
``

Ubuntu users may also install the prebuilt rtl8821ce-dkms package, an older version of the driver maintained by the Ubuntu MOTU Developers group for bionic, eoan and focal. It has been known to work in cases where the newer 






