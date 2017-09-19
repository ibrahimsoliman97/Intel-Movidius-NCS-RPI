# Movidius-NCS-RPI
Object classifier using Movidius Neural Compute Stick with Raspberry Pi and ( Pi Camera or USB Web Camera)

# Required Materials
 1- Movidius™ Neural Compute Stick 
 
 2- Development computer running Ubuntu 16.04 LTS
 
 3- Raspberry Pi 
 
 4- USB Camera 
 
 5- Pi Camera
 
# Installation and running your network with USB Camera on RPI
 Please follow the installation guide provided by Movidius NCS :
 
 https://ncs-forum-uploads.s3.amazonaws.com/ncsdk/MvNC_SDK_01_07_07/NCS_Getting_Started_1.07.07.pdf
 
 https://www.youtube.com/watch?v=f39NFuZAj6s


# Pi Camera Example

![Alt text](/src/connection.jpg?raw=true "Optional Title")

 1- From previous steps, you should have the following files on your Raspberry Pi :
 
    - ncapi folder that include network's floders with each network graph file that has been compiled on your development computer.
    - installed GStreamer on your Raspberry Pi
    
 2- Install GStreamer element for the Raspberry Pi camera module : 
 
 https://github.com/thaytan/gst-rpicamsrc
 
gst-rpicamsrc testing, run command below on your terminal, you should get a live stream from your PiCamera:

    gst-launch-1.0 rpicamsrc bitrate=1000000 fullscreen=0 ! video/x-h264,width=640,height=480,framerate=25/1 ! filesink location=test.h264

 
 3- Download and copy the new python script 'stream_infearnew.py' to '../ncapi/py_examples/stream_infer/'
 
 4- Run stream_infearnew.py
 
SqueezeNet Inference :

FPS >= 8  :

<table>

<tr>
<td align="center" valign="center">
<img src="/src/keyboard.png" alt="description here" />
</td>

<td align="center" valign="center">
<img src="/src/mouse.png" alt="description here" />
</td>
</tr>

<tr>
<td align="center" valign="center">
<img src="/src/lock.png" alt="description here" />
</td>

<td align="center" valign="center">
<img src="/src/watch.png" alt="description here" />
</td>
</tr>

<tr>
<td align="center" valign="center">
<img src="/src/glasses.png" alt="description here" />
</td>
</tr>

</table>


# Acknowledgement
The authors would like to thank the developers of Movidius NCS and gst-rpicamsrc.




<table width="500" border="1" cellpadding="5">

<tr>

<td align="right" valign="right">
This repository has created by IBRAHIM SOLIMAN under DR. LIM KIM CHUAN, Research Lab III, Faculty of Electronic and Computer Engineering, Universiti Teknikal Malaysia Melaka (UTeM).
</td>

<td align="left" valign="left">
<img src="http://www.utem.edu.my/portal/image/newlogo/LogoJawi.png" alt="description here" />
</td>


</tr>

</table>

