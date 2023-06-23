# HOW TO DOWNLOAD YOUTUBE VIDEO WITH PYTHON
# INSTALL PYTUBE BY TYPING pip install pytube

#this is the code you will use to download the video
from pytube import YouTube

yt = YouTube(" YOU WILL PUT YOUR YOUTUBE LINK HERE!!!")

streams = yt.streams.filter(progressive=True, file_extension='mp4').order_by('resolution').desc()

video = streams.first()

video.download()
