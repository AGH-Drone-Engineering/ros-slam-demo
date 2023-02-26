FROM ros:melodic

RUN apt-get update && \
    apt-get install -y ros-melodic-video-stream-opencv && \
    rm -rf /var/lib/apt/lists/*

COPY video.launch /video.launch

CMD [ "roslaunch", "/video.launch" ]
