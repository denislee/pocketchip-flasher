# pocketCHIP-docker-flasher
pocketCHIP docker image to flash correctly

build your docker image:

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
