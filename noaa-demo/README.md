This Dockerfile builds off of the `mbjoseph/earthlab-r` image, fetching the analysis repo from github and then conducting the analysis.
Because data is acquired from a private S3 bucket, it is necessary at runtime to provide Amazon Web Services credentials, e.g.,

```
docker run -e AWS_ACCESS_KEY_ID=$AWS_ACCESS_KEY_ID -e AWS_SECRET_ACCESS_KEY=$AWS_SECRET_ACCESS_KEY mbjoseph/noaa-demo
```

This will only work if you have environmental variables defined for your credentials (i.e., `$AWS_SECRET_ACCESS_KEY exists`).
You can also input the actual keys instead of using environmental variables.
