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

add repository

```
sudo apt-add-repository ppa:caffeine-developers/ppa
sudo apt-get update
```

Then install caffeine by typing in a terminal:
```
sudo apt-get install caffeine
```
