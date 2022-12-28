FROM mambaorg/micromamba:1.1.0-jammy-cuda-11.7.1
COPY --chown=$MAMBA_USER:$MAMBA_USER env/dev.yml /tmp/env.yaml
RUN micromamba install -y -n base -f /tmp/env.yaml && \
    micromamba clean --all --yes

ARG MAMBA_DOCKERFILE_ACTIVATE=1  # (otherwise python will not be found)
