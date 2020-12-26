   ## ToolBox

https://github.com/ventoy/Ventoy/releases - USB multiboot solution

https://sergeistrelec.ru/  - WinPE with multitools

https://github.com/ChrisTitusTech/win10script


   ## Installing RTL8821CE Network Controller
 
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
