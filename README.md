# ci-grafana-image

Docker container from the OSS version of Grafana.

In the spirit of Test Driven Development, a small (<10 seconds) GitHub 
action that tests the Dockerfile with a Preliminary Build Confidence Check 
on each PR to check that it does actually build. This helps by,
- providing fast feedback so that you can fix any issues without 
  needing to wait for others to review.
- mitigating the risk of any local environment idiosyncrasies.
- improving PR reviewer confidence in the change.
- removing the need for PR reviewers to `pull` and `build` locally.


## Building the image
Run the following command in this folder to build a new image:

```
docker build -t ci-grafana-image -f ./Dockerfile .
```

## Running a container
This will start a container using the previously built image and keep it open in interactive mode.

```
docker run -it --rm ci-grafana-image
```

## Deleting the image
View all images to find the image ID

```
docker images
```

Delete the image using the image ID.

```
docker rm [ID]
```
