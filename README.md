# Experimental Deep Learning Development Container
# Planned Usage
Use the pre-built container together with VSCode remote containers to set up
dev environments on remote virtual servers for GPU compute, rather than having
to individually set up the dev environment each time.

## With VSCode
Requirements
* VSCode Dev Containers
* `nvidia-cuda-toolkit` for GPU usage

Using the .devcontainer.json specification, can open a folder using the
dev container, which will build the image according to the Dockerfile and
.devcontainer.json specification.

## Using Jupyter
Works with opening the parent folder with VSCode Dev Containers, following build
and activation, jupyter works from creating a `.ipynb` file and opening with
VSCode.

# Build
`docker build -f docker/Dockerfile .`

# Run in Detached Mode
`docker run -dt --gpus all ghcr.io/chang-alan-l/dl-dev:latest` or use the relevant tag.
Attach with `docker exec -it $CONTAINER_ID /bin/bash`

# TODOs
- [ ] Test pulling the image from the DockerHub or other repository on remote
machine
- [ ] Requirements are also a bit different for deployment, or direct training (for example the entrypoint will be the python binary, with train.py or
infer.py as the command. Might also use `cog` for this purpose.)
- [ ] Expose correct ports for `wandb`?

