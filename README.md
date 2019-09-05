# Intel Movidius NCS RPI
Image classifier and Object detection using Intel Movidius Neural Compute Stick with Raspberry Pi and ( Pi Camera or USB Web Camera)

# Required Materials
 1- Intel Movidius™ Neural Compute Stick 
 
 2- Development computer running Ubuntu 16.04 LTS
 
 3- Raspberry Pi " Raspberry Pi 3 Model B Rev 1.2 has been used in this work "
 
 4- USB Camera 
 
 5- Pi Camera
 
# Installation and running your network with USB Camera on RPI
 Please follow the installation guide provided by Intel Movidius NCS :
 
 https://ncs-forum-uploads.s3.amazonaws.com/ncsdk/MvNC_SDK_01_07_07/NCS_Getting_Started_1.07.07.pdf
 
 https://www.youtube.com/watch?v=f39NFuZAj6s


# Pi Camera Example

![Alt text](/src/connection.jpg?raw=true "Optional Title")

 1- From previous steps, you should have the following files on your Raspberry Pi :
 
    - ncapi folder that include network's floders with each network graph file that has been compiled on your development computer.
    - installed GStreamer on your Raspberry Pi
    
 2- Install GStreamer element for the Raspberry Pi camera module (gst-rpicamsrc): 
 
 https://github.com/thaytan/gst-rpicamsrc
 
gst-rpicamsrc testing, run command below on your terminal, you should get a live stream preview from your PiCamera:

    gst-launch-1.0 rpicamsrc bitrate=1000000 fullscreen=0 ! video/x-h264,width=640,height=480,framerate=25/1 ! filesink location=test.h264

 
 3- Download and copy the modified python script 'stream_infearnew.py' to '../ncapi/py_examples/stream_infer/'
 
 4- Run stream_infearnew.py
 
SqueezeNet Inference :

FPS ~= 9 :

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


# Object Detection [Tiny YOLO V1] :
Compile .prototxt and corresponding .caffemodel to get the NCS graph file:

   download pretrained model (.caffemodel):
     
     https://drive.google.com/open?id=1HBbhOwafuanewpcQ2DMpcURDveb2JNYR
     
By using the graph file of tiny YOLO, you will be able to get a result of object detection with [ ~5 FPS using USB 3 port and ~3 FPS using USB 2 port for Intel Movidius NCS]

Single image inference :

    python3 yolo_example.py 1 ../images/person.jpg
 
 ![Alt text](/src/person.png?raw=true "Optional Title")
 ![Alt text](/src/cat.png?raw=true "Optional Title")


Camera stream inference :

    python3 object_detection_app.py
 
  ![Alt text](/src/tv.png?raw=true "Optional Title")


# Acknowledgement
The author would like to thank the developers of Intel Movidius NCS, YOLONCS and gst-rpicamsrc.




<table>

<tr>

<td align="lef" valign="left">
The equipment used in this work is provided by Machine Learning and Signal Processing Research Lab, Faculty of Electronic and Computer Engineering, Universiti Teknikal Malaysia Melaka (UTeM).
</td>

<td align="right" valign="right">
<img src="https://www.utem.edu.my/image/newlogo/LogoJawi.png" alt="description here" />
</td>


</tr>

</table>

