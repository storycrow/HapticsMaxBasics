# Instructions for VR Gestural Control of Haptics Parameters
## Getting tracking data from an HTC Vive with Max to send to haptics sound patches
#
### You will need a Windows machine to run the HTC Vive via STEAM
##
### DOWNLOAD STEAM 
### https://store.steampowered.com/
##
### SET UP AN ACCOUNT
### You may need to install STEAMVR separately:
### https://store.steampowered.com/app/250820/SteamVR/
##
### Right Click on STEAMVR window to bring up menu, first item should be room setup
##
### Download Windows version of Max 8:
### https://cycling74.com/downloads
##
### Install, then open application, which will automatically generate a folder called Max 8 in My Documents, visible in the File Explorer.
##
### Download Worldmaking package here:
### https://github.com/worldmaking/Max_Worldmaking_Package
##
### In the File Explorer:
### Move package ZIP to My Documents/Max 8/Packages
### Unpack by selecting the folder and clicking “Extract All”
### Make sure to move the unpacked ZIP file back to the level of My Documents/Max 8/Packages (not inside another subfolder).
##
### Make sure Max is off, STEAM is on (w/ room setup configured + tracking station cameras on/working) before opening Max.
##
### In Max, go to File/ New Patcher.
### Make sure the Lock icon in the bottom lefthand corner is unlocked.
### Click on the middle of the patcher, hit hotkey N to bring up a new object, left click inside the object to bring up a cursor, type “htcvive.”
### Click outside and hover over the left corner of the object until you see a yellow arrow, click on it and select “help.”
### In the help patcher double click on the object called “tracking” that is attached below the htcvive object in the middle.
### Double click on “all-tracking-data.”
### There you can see if the tracking data is working.
##
### You can send the tracking data to another patcher using send and receive objects. To create a new object, press hotkey N. 
### To send info, type s followed by a unique address, for example “s LeftController_X_Position.” Connect a patch cord between the outlet of the value you’d like to send and the inlet of your send object. 
### In the sound patch, you can “receive” the value and use it to control whatever parameter you’d like.
### To receive info, type r followed by your unique address, in our example “r LeftController_X_Position.” 
### Connect a patch cord between the outlet of your receive object and the inlet of the variable you’d like to control. 
##
### TIP:
### A “scale” object can help you tailor the range of your data to the relevant range of your target variable. For example, the relevant x position of the left controller might be in the range of -2.5 to 1.5 when you move the controller around your space. Perhaps you are wanting to control the frequency of a sine wave oscillator from 100 to 102 Hz (to create frequency beating with a second oscillator fixed at 100 Hz). In this case you would write “scale -2.5 1.5 100. 102.” (without the quotation marks) to scale the data accordingly.
