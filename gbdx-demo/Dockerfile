FROM mbjoseph/earthlab-r

# acquire source files from gitlab
RUN mkdir -p /home/noaa\
  && cd /home/noaa\
  && wget https://gitlab.com/mbjoseph/gbdx-demo/repository/archive.zip?ref=master\
  && unzip archive.zip?ref=master\
  && mv gbdx-demo-master* noaa-demo\
  && rm archive.zip?ref=master

# load EPA ecoregion data
RUN mkdir -p /home/noaa/noaa-demo/data/ecoregions\
  && cd /home/noaa/noaa-demo/data/ecoregions\
  && wget ftp://ftp.epa.gov/wed/ecoregions/co/co_eco_l4.zip\
  && unzip co_eco_l4.zip\
  && rm co_eco_l4.zip

# load USGS hydrology data
RUN mkdir -p /home/noaa/noaa-demo/data/hydrology\
  && cd /home/noaa/noaa-demo/data/hydrology\
  && wget ftp://rockyftp.cr.usgs.gov/vdelivery/Datasets/Staged/Hydrography/NHD/State/MediumResolution/Shape/NHD_M_08_Colorado_ST.zip\
  && unzip NHD_M_08_Colorado_ST.zip\
  && rm NHD_M_08_Colorado_ST.zip
