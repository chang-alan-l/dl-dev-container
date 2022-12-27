# Experimental Deep Learning Development Container
# Usage
Currently the plan is to use the pre-built container together with VSCode remote
containers.

Possible other use case is to set up dev environments on remote virtual servers
for GPU compute, rather than having to individually set up the dev environment
each time.

# Build
`docker build -f docker/Dockerfile .`

# TODOs
- [ ] For development, it's likely that the container itself needs git and other
dev tools depending on the workflow.
- [ ] Test pulling the image from the DockerHub or other repository on remote
machine
- [ ] Requirements are also a bit different for deployment, or direct training
- for example the entrypoint will be the python binary, with train.py or
infer.py as the command. Might also use `cog` for this purpose.

