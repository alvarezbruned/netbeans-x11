Netbeans-x11

docker run -td \
    --net host \
    --cpuset-cpus 0 \
    -v /tmp/.X11-unix:/tmp/.X11-unix \
    -e DISPLAY=unix$DISPLAY \
    -v $HOME/Downloads:/root/Downloads \
    --device /dev/snd \
    -m 500000000 \
    --memory-swap 2500000000 \
    -v /dev/shm:/dev/shm \
    --name netbeans-x11 \
    albertalvarezbruned/netbeans-x11
