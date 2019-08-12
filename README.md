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

# turn on caffeine

Disable suspend and hibernation

For systems which should never attempt any type of suspension, these targets can be disabled at the systemd level with the following:

```
sudo systemctl mask sleep.target suspend.target hibernate.target hybrid-sleep.target
```

To re-enable hibernate and suspend use the following command:

```
sudo systemctl unmask sleep.target suspend.target hibernate.target hybrid-sleep.target
```
