FROM mbjoseph/earthlab-r

RUN mkdir -p /home/noaa\
  && cd /home/noaa\
  && wget https://github.com/ResearchComputing/noaa-demo/archive/master.zip\
  && unzip master.zip\
  && mv noaa-demo-master noaa-demo

ENTRYPOINT make -C /home/noaa/noaa-demo
