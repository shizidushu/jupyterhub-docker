FROM jupyterhub/jupyterhub:1.0.0


# APT packages
RUN apt-get update && \
    apt-get install  -y \
    git \
    wget \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# COPY jupyterhub_config.py .

RUN wget https://raw.githubusercontent.com/jupyterhub/jupyterhub/1.0.0/examples/cull-idle/cull_idle_servers.py

RUN pip install \
    jupyter-client==6.1.2 \
    dockerspawner==0.11.1 \
    oauthenticator==0.11.0 \
    && pip install --upgrade https://github.com/jupyterhub/nativeauthenticator/tarball/master