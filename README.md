# moobs-studio
Docker linux container for OBS Studio (nvidia GPU enabled) for cloud and selfhosting

the image will be around 4.5GB (keep in mind that you will have a linux desktop available for your own convenience) and there are a lot of dependencies, so I cannot really shrink the size

This setup was tested on a windows machine using WSL (Ubuntu 20.04) and NVIDIA Cuda for docker activated

On a native linux environment NVIDIA HW acceleration is even easier to use

For cloud setup I cannot post any hints, because I do not have any cloud setup and also this may be different depending which cloud environment you use.
But you will defnitely need some NVIDIA GPU supported

You can access OBS-Studio via browser using novnc accessing your personal LXDE Desktop
It comes with integrated Obs-Websocket for streaming have a look at another Project of mine: [streaming](https://github.com/moo-the-cow/streaming)

Because this is specifically for streaming there will be a preset of scenes (especially the LIVE scene having the srt setup from my other project). Feel free to change the backgrounds for BRB etc.

# HOWTO
You can access the Desktop via Browser url: http://[hostip]:6080/ if you want to access another port just modify the ports in your docker-compose yaml file.
