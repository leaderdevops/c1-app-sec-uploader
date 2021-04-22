# c1-app-sec-uploader

This demo app for Cloud One Application Security create an Apache PHP based front end allowing to upload kind of files. It is to simulate file uploading capabilities from real world web applications.

Application Security integration done via the provided Dockerfile.

## Usage

First, clone the repo

Then build and run the container

```sh
# Build the image
docker build -t uploader .

# Run the container
docker run \
  --rm -p 80:80 \
  --name uploader \
  -e TREND_AP_KEY=<YOUR APP SEC GROUP KEY>
  -e TREND_AP_SECRET=<YOUR APP SEC GROUP SECRET>
  uploader
```

The upload app is accessible on port 80.

Finally, upload malicious files.

## Jenkins

An example Jenkins pipeline is provided to integrate this app to your Jenkins instance.
