# RnderWare Graphics SDK and RenderWare Studio setup guide
## Configuring a VirtualBox virtual machine
1. Downaload VirtualBox 6.0.2.4 for your system [here](https://www.virtualbox.org/wiki/Download_Old_Builds_6_0) and install it.
   > We need the older version of VirtualBox in order to use 3D acceleration in Windows XP
2. After the installation open the installed VirtualBox and create a new VM. Name it as you want. Under `Type` select `Microsoft Windows`, under `Version` select `Windows XP 32-bit`.
3. Click `Next`. Assign as much RAM as you want for a VM tohave. Click on `Next` again. Tick `Create Virtual Hard Disk Now`. Click `Create`. Select `VDI` and click `Next`. In the next dialogue select `Dynamically allocated` and click on `Next` yet again. Your virtual disk image will be saved in the directory of a VM by default, better leave it as it is. Drag a slider to adjust the amount of space on a virtual disk. As it is allocated dynamically, you can select something like 500GB to have no extra troubles in future. After you are done, hit `Create`.
4. Now click on `Settings`, select `System` on the left hand side, drag a `Video Memory` slider up to it's limit of 128MB. Make sure `VBox VGA` is selected under the `Graphics Controller`. And at the end, tick `Enable 3D Acceleration` **(IMPORTANT)**
5. Go under `Storage`, click on the optical drive marked as `Empty`. On the right side you will see the CD icon with a little arrow below it, click on it and select *Windows XP* ***.iso*** file which you can download [here](https://archive.org/details/WinXPProSP3x86).
> Here was a lot of text, but a small amount of actions. We are done tweaking the VM now.
## Configuring the operating system
1. After you finished setting up a VM, click `Start`. VirtualBox will now load up the machine from a mounted Windows XP .iso
2. Wait while installer is loading up, then just follow the onscreen instructions. Press F8 to accept the Licence Agreement, then make sure that `Unpartitioned space` is selected under the install destionation. Select `Format the partition using the NTFS file system <Quick>` to format the partition faster.
3. After some steps installer will reload the machine and then continue the installation with some graphical interface.
4. Here you will be asked to select language preferences and keyboard layouts, select english everywhere and click `Next`. You will be asked to insert user and organization name. Type in whatever you want into those fields. You can leave `Organization Name` blank if you want. On the administrator configuration screen you can leave a password field blank as well.
5. Then you will be prompted to insert the product key. You can use one from the [page where you downloaded the Windows .iso](https://archive.org/details/WinXPProSP3x86).
6. After some more installation steps the window will pop up, asking your network preferences. Select `Typical` under connection type.
7. The machine will reload one more time, this time showing you some welcome screens that Microsoft prepared for their customers. After which you will be asked to select the protection level of your system. Select no protection options there and also click on `Skip` during the network configuration step thereafter. On the next screen, system will ask you to register a MS account, ignore it also, by selecting `No, not this time`.
8. Wait while Windows will load up fully (it will open the *Start* menu thereafter). Then click `Devices` on the VirtualBox' title bar, mark on `Optical Drive` and deselected the inserted Windows installation disk.
9. Restart the machine and start hitting F8 during the startup process. In the opened prompt select `Safe mode` (navigate using arrow keys). Windows will now be loaded in safe mode.
10. Select the `Administrtator` account, and click `Yes` in a warning prompt after system full load. Select `Devices` on the window title bar again, the click `Insert Guest Additions CD image` from dropdown. VirtualBox will now mount a CD to a machine which will open up an installation prompt. Click `Next` to continue the setup, tick `Direct3D Support` on the next screen of an installer and begin the installation by following some onscreen instructions. During the installation a warning will come up several times, on those windows click `Continue Anyway`. After the installation tick `Reboot now` and click `Finish`. Machine will now reboot into Windows normally.
> And with that done, we finally have your machine ready to meet RenderWare
## Installing the software
1. Create a folder on your real system somewhere and name it somehow like *Shared folder*.
2. On the VirtualBox window header select `Machine -> Settings -> Shared Folder`. Click the folder icon with a plus sign on the right side of a window and select the folder you just created.
3. Download [Microsoft ActiveX Control Pad](https://docs.microsoft.com/en-us/previous-versions/ms968493(v=msdn.10)) and put into the *Shared Folder* (on your real hardware).
4. Download [RenderWare Studio and RenderWare SDK files](https://www.mediafire.com/file/nxe7pfwf645hnzz/Web_Archive_Extracted.zip/file) ([source](https://archive.org/details/renderwaregraphics3.7sdkandstudio2.01)) and put downloaded .zip file to the *Shared Folder* as well.
5. On a Virtual Machine go `Start -> My Computer -> Shared Folder`. Drag-and-drop the files from it to the VM's desktop.
6. Execute `setuppad.exe` and install it.
7. Extract `Web Archive Extracted.zip` by right clicking on it and selecting `Extract all...`.
8. Navigate to `Renderware Studio2.01 NoLicense.rar \ Studio` and execute the `setup.exe`.
9. Follow all the instructions and leave all the fields as they set by default. Continue to the final step, where it will say `Start RenderWare studio` and go tutorial to the next step, leaving the installer opened.
10. Navigate back to the root of downloaded content and then go under `RenderWareStudioCrack` and copy the .dll laying here.
11. Now go to `C: \ RW \ Studio \ Programs` and paste the copied .dll here replacing the original one.
12. Go back to installer and click `Finish`. RenderWare Stdio should open up now. 
    > Now let's install the RW Graphics SDK as it contains some useful tools
13.  Navigate to `Renderware Graphics3.7sdkandstudio2.01.rar \ Renderware Studio 3.7 SDK for Windows.rar \ Renderware 3.7 SDK (For Windows) Full \ Renderware Graphics SDK 3.7` under the downloaded extracted .zip and execute the `setup.exe` here.
14. Follow the onscreen instructions to install the SDK and finish the setup by deselecting the `Check changelog and website` at the end.
15. Navigate to the `License` folder in a parent folder of ` Renderware Graphics SDK 3.7` and copy the file laying here. Go to `C: \ RW \ shared \ openexport \ bin` and replace the existing file by pasting the one you just copied.
