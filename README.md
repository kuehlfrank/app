# Kühlfrank-app
This is the main repository from which you can run the full stack.


## Docker
### Running with docker
Running with docker is very simple. All you need is docker and docker-compose
```sh
docker-compose pull # update local images
docker-compose up -d # run all needed containers in background
```
This will start the webapp on [http://localhost:3001](http://localhost:3001)

### Building with docker
This will use the local files to make a new docker image instead of pulling one from the specified registry.
```sh
docker-compose build
docker-compose up -d
```
Optionally specify `--parallel` after `docker-compose build` for faster builds.

### Remakrs
Changing the port of the `backend` container is currently not possible because the value is hard coded into `.env.docker` in the frontend.

## Submodules
init (after clone)
```sh
git submodule update --init --recursive
```
update all submodules with
```sh
git submodule -q foreach git pull -q origin main
git add .
git commit -m "update submodules"
git push
```
