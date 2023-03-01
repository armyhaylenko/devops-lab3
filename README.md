# DevOps lab 3

## The app
The app is a simple node js app from express template.

## Building
I used `docker build -t theirshadow/my-nodejs-app .` to build the image.

## Pushing
I used `docker image push theirshadow/my-nodejs-app:lab3` to push the image to my repo.

## Running
To run locally, run `npm i && npm run start`.
To run in a docker container, use
```shell
docker pull theirshadow/my-nodejs-app:lab3 && \
docker run --memory=1g --cpus=2 -p 80:3000 \
--name my-nodejs-app-container theirshadow/my-nodejs-app:lab3
```

## Verifying correctness
Use
```shell
curl http://localhost && curl http://localhost/users
```
Or visit those addresses in your browser (no port specified since the default http port is 80)
