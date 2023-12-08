live camera recording using rstp
gst-launch-1.0 -e -v tcambin serial=31220061 location=rtsp://128.3.2.1:5000/live ! 'video/x-bayer,format=(string)rggb,width=(int)1920,height=(int)1080,framerate=(fraction)30/1' ! bayer2rgb ! videoconvert ! x264enc tune=zerolatency ! qtmux ! filesink location=output_video.mp4
