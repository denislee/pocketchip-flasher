# pocketCHIP-docker-flasher
pocketCHIP docker image to flash correctly

---

# build your docker image:

```
docker build -t flash:1 .
```

run your docker imagem mapping your device:

```
docker run -it --privileged -v /dev:/dev flash:1 bash
```

then, just run the script

```
cd Flash-CHIP
./Flash.sh
```

or you may your an already made image: `denislee/pocketchip-flasher`


https://medium.com/@0x1231/nextthingco-pocket-c-h-i-p-flashing-guide-3445492639e


---

# disable screen saver

Firstly, you may need to install xset, a lightweight application that controls some X settings.

```
apt-get install x11-xserver-utils
```

Now open up your ~/.xinitrc file (if you don't have one then create it) and enter this:

```
xset s off         # don't activate screensaver
xset -dpms         # disable DPMS (Energy Star) features.
xset s noblank     # don't blank the video device

exec /etc/alternatives/x-session-manager      # start lxde
```

This file runs once every time X starts and should solve the problem. I copy and pasted it from my own .xinitrc and can confirm that my screen does not blank.
