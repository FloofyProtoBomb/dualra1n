# what is ?

this is a tool to dualboot your idevice, dualboot means having 2 version of ios on just one device. this is semi-untethered means that if you are for example on ios 14.3 with the dualboot when you reboot you come back on the normal ios that you had for me was 15.7 

# dualboot-ios-15-with-14-script palera1n's younger brother
to do this on linux, your device would have to have 16 gb of space free because the proccess is different when the dualboot is alrady installed that would be 12gb however to do on macos you would have to have only 12 gb to do it correctly. i recommend doing on macos  

this is a script to dualboot your iphone on ios 15 with 14 that work only for a8-a11 (checkm8 devices)

iphone 6s and 6s+ work very nice
iphone 7 and 7+ work however home button does not work yet but there are tweak that you can use as a iphone x so you dont have to use button
iphone 8 and 8+ does not tested yet but i supposed this work like iphone7
iphone x work but touch does not work yet
works on ipad too but i wont say all ipad so a8-a11 

# now you can use MACOS and linux remember with sudo.

# tutorial

Options: example ./dualboot.sh --dualboot 14.3 

    --dualboot          dualboot your device ios 15 with 14 
    
    
    --jail_palera1n uses only if you have the palera1n jailbreak semi-untethered installed, it will create partition on disk + 1 because palera1n create a new partition. disk0s1s8 however if you jailbreakd with palera1n the disk would be disk0s1s9", for example ./dualboot.sh --dualboot 14.3 --jail_palera1n 
    
    
    --jailbreak         jailbreak your second ios. you can use it when your device boot correctly the second ios. example ./dualboot.sh --jailbreak 14.3

    --taurine           this will install the jailbreak of taurine. ./dualboot.sh --jailbreak 14.3 --taurine 
   
    --help              Print this help
  
      --jump            that will bypass to second ios in case that you dont know the password of icloud however you could not login on icloud, but you can login on appstore and download apps. just use that in case that you dont remember the password, thank you for share mobileactivationd @MatthewPierson". example./dualboot.sh --jump 14.3 in case that you want to restore icloud use --jump 14.3 --back
     
     --getIpsw           using this will download a ipsw of your version which you want to dualboot. ./dualboot.sh --getIpsw 14.3

    --dfuhelper         A helper to help get A11 devices into DFU mode from recovery mode
    
    --boot              put boot alone, to boot your second ios. /dualboot.sh --boot
    
    --dont_createPart   Don't create the partitions if you have already created. ./dualboot.sh --dualboot 14.3 --dont_createPart
    
    --restorerootfs     Remove partitions of dualboot. ./dualboot.sh --restorerootfs
    
    --fix_preboot       that restore preboot with the prebootBackup. --fix_preboot
    
    --debug             Debug the script

Subcommands:
    clean               Deletes the created boot files




important if you have palera1n semi-tethered jailbreak always put --jail_palera1n always 

1: download your ipsw and put it on ipsw/ directory (you can download of ipsw.me. please only ios 14.* also please download exactly your ipsw for your device) (your ios version that you want to dualboot with also is recommended ios 14.3 because you can jailbreak with taurine)

2: execute ./dualboot --dualboot 14.3 (the version of your ipsw downloaded which is the version that you want to dualboot ) 

3: ./dualboot --boot 


# other options

to download the ipsw you can use --getIpsw that will download the ipsw however you must have installed brew if not, you have to download manual
after that boot and finished to dualboot you can jailbreak it using --jailbreak 
screen blue and does not boot for example using --dualboot 14.3 --dont_createPart --fixBoot that will fix the boot files after that boot it and that will boot well


---
# just in case kenelpanic
in case that your iphone not boot on the second ios try to do this:
you will have to record a video of iphone's screen because you have to note the name of the preboot directory when that is booting. 



https://user-images.githubusercontent.com/85508740/205308846-edc2673f-4e8c-4265-a63b-14664e4301db.MOV


so you will see that is booting however that will reboot because the preboot directory is not created so we have to create it. 
you have to record a video which look like above. after you have take a photo or to note the name of the directory 

![IMG_0774](https://user-images.githubusercontent.com/85508740/205313633-567ff020-1279-4fdc-88b1-bc0914bdda82.jpg)

like this so note the name /private/preboot/*thisName*/usr/standalone/firmware
now boot ./sshrd.sh or any ssh ramdisk after execute mount_filesystem, execute mount_apfs /dev/disk0s1s10 /mnt4/ after that execute mkdir "*thisName*" | mkdir "*thisName*"/usr | cp -av /mnt6/"theonlydirectorythatexist"/usr mnt4/"*thisName*"/
reboot and your iphone should boot without error 
---
# how to jailbreak 
---
to jailbreak your device: ./dualboot.sh --jailbreak 14.3 (or your version) remember that if you have palera1n semitethered jailbreak you have to put --jail_palera1n
that will jailbreak your dualboot on whatever version, installing pogo app just open it and press install after press do all and that will respring and you will have sileo and substrate 

however if you want taurine just use this command ./dualboot.sh --jailbreak 14.3 --taurine (if you have palera1n jailbreak use --jail_palera1n)
first install trollstore opening tv app so after that open trollstore and press (rebuild icon cache) after that taurine will be showed now open taurine and press on the button jailbroken when that reboot you are ready to install tweaks, never open or press jailbroken on taurine again, each time that you reboot and boot to second ios you have to reinstall libhooker opening sileo and press reinstall libhooker

---

for any error you could create issues 

test it on iphone 6s on ios 15.7 using macos big sur and on kali linux

# thanks

THANKS PALERA1N,nathan for beautiful ramdisk,https://dualbootfun.github.io/ for the knowdlege, MatthewPierson, Ralph0045, people who help me test on discord like @something, @samm and others and @fatih to help me give support on linux and all people who created the boot patcher tool, thank @darlinghq for the amazing emulator,thank @blacktop. thank https://github.com/dora2-iOS for fix button. thanks all.

