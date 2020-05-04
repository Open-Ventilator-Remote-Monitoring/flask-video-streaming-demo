### Video Streaming from webcam to dashboard

## Set up the camera

### Clone Miguel Grinberg's repo:
git clone https://github.com/miguelgrinberg/flask-video-streaming

### Install opencv
- sudo pip3 install opencv-python

### Install all the requirements files: 
- sudo pip3 install -r requirements.txt
- sudo pip3 install -r requirements-opencv.txt
- sudo pip3 install -r requirements-pi.txt
- sudo pip3 install opencv-python==3.4.2.16

### Set the environment variable
`export CAMERA=opencv` or `export CAMERA=pi`

### Enable the camera
- If you’re using a camera, enable it in raspi-config and then reboot

### Install these dependencies:
I also had to install a bunch of addtional dependencies to get the camera to work in opencv
https://stackoverflow.com/questions/53347759/importerror-libcblas-so-3-cannot-open-shared-object-file-no-such-file-or-dire
- Sudo apt-get install libatlas-base-dev
- pip3 install opencv-python 
- sudo apt-get install libcblas-dev 
- sudo apt-get install libhdf5-dev 
- sudo apt-get install libhdf5-serial-dev 
- sudo apt-get install libatlas-base-dev 
- sudo apt-get install libjasper-dev 
- sudo apt-get install libqtgui4 
- sudo apt-get install libqt4-test
- In addition, I also needed to install libilmbase-dev libopenexr-dev libgstreamer1.0-dev libavcodec-dev libavformat-dev libswscale-dev and libwebp-dev
So many dependencies!

### Resize the image in camera_opencv.py 
Follow these directions: https://stackoverflow.com/questions/43315349/how-to-resize-frames-from-video-with-aspect-ratio

Forked from Miguel Grinberg's flask-video-streaming repo:
[video streaming with Flask](http://blog.miguelgrinberg.com/post/video-streaming-with-flask) and its follow-up [Flask Video Streaming Revisited](http://blog.miguelgrinberg.com/post/flask-video-streaming-revisited).
