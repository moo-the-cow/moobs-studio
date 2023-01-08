## you might also wanna check out related projects:
+ [streaming](https://github.com/moo-the-cow/streaming): SRTLA-RECEIVER and SRTLA-NGINX for self hosting
+ [moobs](https://github.com/moo-the-cow/moobs): bot for obs websocket and twitch (and more => see wiki)

# moobs-studio
Docker linux container for OBS Studio (nvidia GPU enabled) for cloud and selfhosting

the image will be around 4.5GB (1.48GB compressed - keep in mind that you will have a linux desktop available for your own convenience) and there are a lot of dependencies, so I cannot really shrink the size

This setup was tested on a windows machine using WSL (Ubuntu 20.04) and NVIDIA Cuda for docker activated
+ https://docs.nvidia.com/cuda/wsl-user-guide/index.html
+ https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html

On a native linux environment NVIDIA HW acceleration is even easier to use

(have a look in the docker-compose yaml file comments)

For cloud setup I cannot post any hints, because I do not have any cloud setup and also this may be different depending which cloud environment you use.
But you will defnitely need some NVIDIA GPU passed through for your container

You can access OBS-Studio via browser using novnc accessing your personal LXDE Desktop
It comes with integrated Obs-Websocket for streaming have a look at another Projects of mine: [streaming](https://github.com/moo-the-cow/streaming) and [moobs](https://github.com/moo-the-cow/moobs)

Because this is specifically for streaming there will be a preset of scenes (especially the LIVE scene having the srt setup from my other project). Feel free to change the backgrounds for BRB etc.

**if you are not a developer please contact a someone who's familiar with this, that person will know what to do**

you pick yourself if you want to enable/disable the overlay so this gets promoted/spread, but I'd very much appreciate it (especially at the start of this project)

# Changelog
+ v1.3: updated OBS to version 29.0.0
+ v1.2: updated OBS to version 29.0.0 beta 2
+ v1.1: added initial scene and profiles
+ v1: updated ffmpeg and srt

# HOWTO
You can access the Desktop via Browser url: http://[hostip]:6080/ if you want to access another port just modify the ports in your docker-compose yaml file.

# SETUP
just because I have documented how to use docker-compose yaml files I will just quickly post an example:

download all the files into a directory and start it via 

`docker-compose -f docker-compose.yaml up -d`

I recommend you add the docker compose services from https://github.com/moo-the-cow/moobs and https://github.com/moo-the-cow/streaming (streaming folder) into your docker-compose yaml file for the ultimate streaming experience (communicating within their docker subnet). Those services are well documented on those linked pages.

Otherwise you will have to re-configure your Scene and use the url for your own SRT server and also the reconfigure html file showing the bitrate

## Audio
you need to have WSLG and WSL installed (see volume mappings)

# Common Issues
+ I cannot see my stream souce: Check your SRTLA url in the LIVE scene. IP and streamkey must match your SRT endpoint
+ My Websocket connection isn't working: By default websocket is disabled, enable it via checkbox and check the IP and password match the settings of the tool you're connecting from.
+ HEVC for recording doesn't work: Currently recording in HEVC only for windows is supported

# additional words
sorry I haven't created a wiki page yet, there is actually a lot more to document, but I just wanted to release, because it was working for quite a while on my end already. if you have any questions or issues just create a ticket, and IF I can solve it and IF I have time I will get to it.

I'm very curious about your experience with this in a cloud, please let me know if you want to share!

# Screenshots:
![image](https://user-images.githubusercontent.com/34907770/198009476-f77ce5dc-5e8b-4812-9886-165cf377028c.png)
![image](https://user-images.githubusercontent.com/34907770/198009599-4672367f-a3f8-4a73-acb5-c5071a362fb9.png)
![image](https://user-images.githubusercontent.com/34907770/198009630-35e4c77f-b33c-4a03-9f55-7d309c758ef7.png)

