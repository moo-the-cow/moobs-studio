# moobs-studio
Docker linux container for OBS Studio (nvidia GPU enabled) for cloud and selfhosting

the image will be around 4.5GB (keep in mind that you will have a linux desktop available for your own convenience) and there are a lot of dependencies, so I cannot really shrink the size

This setup was tested on a windows machine using WSL (Ubuntu 20.04) and NVIDIA Cuda for docker activated

On a native linux environment NVIDIA HW acceleration is even easier to use

(have a look in the docker-compose yaml file comments)

For cloud setup I cannot post any hints, because I do not have any cloud setup and also this may be different depending which cloud environment you use.
But you will defnitely need some NVIDIA GPU supported

You can access OBS-Studio via browser using novnc accessing your personal LXDE Desktop
It comes with integrated Obs-Websocket for streaming have a look at another Projects of mine: [streaming](https://github.com/moo-the-cow/streaming) and [moobs](https://github.com/moo-the-cow/moobs)

Because this is specifically for streaming there will be a preset of scenes (especially the LIVE scene having the srt setup from my other project). Feel free to change the backgrounds for BRB etc.

**if you are not a developer please contact a someone who's familiar with this, that person will know what to do**

you pick yourself if you want to enable/disable the overlay so this gets promoted/spread, but I'd very much appreciate it.

# HOWTO
You can access the Desktop via Browser url: http://[hostip]:6080/ if you want to access another port just modify the ports in your docker-compose yaml file.

# SETUP
just because I have documented how to use docker-compose yaml files I will just quickly post an example:

download all the files into a directory and start it via 

`docker-compose -f docker-compose.yaml up -d`

I recommend you add the docker compose services from https://github.com/moo-the-cow/moobs and https://github.com/moo-the-cow/streaming (streaming folder) into your docker-compose yaml file for the ultimate streaming experience. Those services are well documented on those linked pages

Screenshots:
![image](https://user-images.githubusercontent.com/34907770/198009476-f77ce5dc-5e8b-4812-9886-165cf377028c.png)
![image](https://user-images.githubusercontent.com/34907770/198009599-4672367f-a3f8-4a73-acb5-c5071a362fb9.png)
![image](https://user-images.githubusercontent.com/34907770/198009630-35e4c77f-b33c-4a03-9f55-7d309c758ef7.png)

