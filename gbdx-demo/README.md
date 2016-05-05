This Dockerfile builds off of the `mbjoseph/earthlab-r` image, fetching the analysis repo from github and then conducting the analysis.
The image is intended to be run in the Digital Globe GBDX environment, which mounts an S3 bucket to /mnt/work/input
