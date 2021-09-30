## Ubuntu installation
Fisrt of all you need at least 100GB of free storage on your drive, an atleast four-GigaByte flash drive, and working PC or laptop, then follow the follwoing steps one by one to do dual boot with your current operating system.
### Download the ISO
Go to [Ubuntu official website](https://ubuntu.com/download/desktop) and dwonload the latest version between the releases.
![image](https://user-images.githubusercontent.com/64384499/134730757-4a0a5e95-6b77-461d-aaa3-e8b717a08cc6.png)
### Burning the ISO
You will need a tool to burn the ISO on your flash drive, I used [Rufus software tool](https://rufus.ie/en/) to burn it.
### Seperate 100GB for the OS
Before going to the installation steps, you need to free up 100GB on your drive, right click on _This PC_ and then press device manager -> storage -> Disk Management, and shrink 100GB form any drive you want.
![11](https://user-images.githubusercontent.com/64384499/135486407-967c47ba-a213-47b7-8789-9158066e889d.PNG)
### Installation steps
1. Now plug-in your flash frive into your PC or laptop.
2. Open Rufus software tool as administrator and select your ISO that your downloaded before, then press start and wait the process to compelete, it may take some time depending on your hardware.

![image](https://user-images.githubusercontent.com/64384499/134745909-bf6851c2-cba0-42d3-ba2d-fbd76f99167a.png) 

3. Now your bootable flash drive is ready to be install, restart your PC or laptop and enter the BIOS menu.
4. Make sure to turn off the _legacy support_, it may differ from one to another but make sure if you have the option of _legacy support_ turn it off, or make the boot mode on _UEFI_.

Solution one             |  Solution two  
:-------------------------:|:-------------------------:
<img src="https://user-images.githubusercontent.com/64384499/134746461-65d8d20f-fda4-425b-906e-718d64fef3fb.png" width="1000" height="300"> |  <img src="https://user-images.githubusercontent.com/64384499/134746636-3a18e9b9-16c9-46db-8b94-b5c165e1210b.png" width="900" height="300">

5. After that save and exit, then Boot your PC or laptop from your flash drive.
6. After Ubuntu installer opened choose install Ubuntu, then you will find some option choose the last option called "somthing else".
7. Now a window like this will open, be carful any mistake may cause to data lose.

![1](https://user-images.githubusercontent.com/64384499/134747542-4f2d59a5-c123-4c9a-8699-da37fa1a87ad.png)

8. Now you need to choose the partion which will you will install Ubuntu, we will use the free space that shrinked before in windows.
9. Right click on the free sapce then _add_, first we need to make the (/boot) the boot file system for Ubuntu, 1GB is enough for that.

![2 (1)](https://user-images.githubusercontent.com/64384499/135488592-549241fd-8609-4408-9f2d-7a9be5caaa12.png)

10. We need to make swap area douple the amount of your phyiscal RAM, I have 8GB RAM, so I will make it 16GB swap area.

![3](https://user-images.githubusercontent.com/64384499/135488886-03835b83-a511-4f23-9bec-a089989f2175.png)

11. You can make (/home) partion or not, its depends on you but I prefer 5GB for that.
12. Now make the root partion for the remaining space.

![4](https://user-images.githubusercontent.com/64384499/135489295-869cf189-e75b-489d-993a-4c1843eaa6b1.png)

13. Now do not forget to choose the _Device for boot loader installation_ for the (/boot) partion you made then press _Install now_.

![5](https://user-images.githubusercontent.com/64384499/135489517-818beb58-8f57-461b-886e-3295e26c1921.png)

14. A pop-up menu will apper confirming on the formation.

![6](https://user-images.githubusercontent.com/64384499/135489816-957ce378-8746-4a6b-97a0-c5b7f2bf9481.png)

15. Compelete the installtion steps till reach the installtion window below and that may take a while depending on your hardware.

![9](https://user-images.githubusercontent.com/64384499/135490064-724607e0-4f77-47f3-a96e-614159eaae0c.png)

### Some issuses you may face
There is an issue you may face after the installtion, the window may start by defualt, to solve this problem, restart your laptop or PC and plug-in ypur flash drive and boot form it to test Ubuntu open the terminal and execute these commands one by one.

```md
sudo apt-add-repository ppa:yannubuntu/boot-repair

sudo apt-get update

sudo apt-get install -y boot-repair

boot-repair
```



