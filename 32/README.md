# Docker wine

## Run

    xhost +si:localuser:$(whoami) >/dev/null

    docker run --rm -it \
      -e DISPLAY \
      -v `pwd`:/root/.wine/drive_c/users/root/Temp \
      -w /root/.wine/drive_c/users/root/Temp \
      -v /tmp/.X11-unix:/tmp/.X11-unix:ro \
      -v /etc/localtime:/etc/localtime:ro \
      splattael/wine:32
