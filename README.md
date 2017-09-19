# Movidius-NCS-RPI
Object classifier using Movidius Neural Compute Stick with Raspberry Pi and ( Pi Camera or USB Web Camera)

# Required Materials
 1- Movidius™ Neural Compute Stick 
 
 2- Development computer running Ubuntu 16.04 LTS
 
 3- Raspberry Pi 
 
 4- USB Camera 
 
 5- Pi Camera
 
# Installtion and running your network with USB Camera on RPI
 Please follow the attached installation guide provided by Movidius NCS :
 
 https://ncs-forum-uploads.s3.amazonaws.com/ncsdk/MvNC_SDK_01_07_07/NCS_Getting_Started_1.07.07.pdf
 
 https://www.youtube.com/watch?v=f39NFuZAj6s


# Pi Camera Example

![Alt text](/src/connection.jpg?raw=true "Optional Title")

 1- From prevouis steps, you sholud have the following files on your Raspberry Pi  :
 
    - ncapi folder that include network's floders with each network graph file that has been compiled on your development computer.
    - installed GStreamer on your Raspberry Pi
    
 2- Install GStreamer element for the Raspberry Pi camera module : 
 
 https://github.com/thaytan/gst-rpicamsrc
 
gst-rpicamsrc testing, run below coommnd on your termainal, you should get a live stream from your PiCamera:

gst-launch-1.0 rpicamsrc bitrate=1000000 fullscreen=0 ! video/x-h264,width=320,height=480,framerate=25/1 ! filesink location=test.h264

 
 3- Use the new python script : stream_infearnew.py
 
FPS >= 8 fps for SqueezeNet :

<table>

<tr>

<td align="center" valign="center">
<img src="/src/keyboard.png" alt="description here" />
<br />
Caption text centered under the image.
</td>

<td align="center" valign="center">
<img src="/src/mouse.png" alt="description here" />
<br />
Caption text centered under the image.
</td>

</tr>

</table>


Network inferance | 
|:-------------------------:|:-------------------------:|
|![](/src/keyboard.png)  |  ![](/src/mouse.png)|
|![](/src/lock.png)      |  ![](/src/watch.png)|


![](/src/glasses.png)   
