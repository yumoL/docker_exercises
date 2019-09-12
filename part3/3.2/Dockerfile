FROM ubuntu:16.04

RUN apt-get update && apt-get install -y \
    python3 python3-pip ffmpeg wget rtmpdump && \
    pip3 install pycryptodome && \
    pip3 install --user --upgrade yle-dl && \
    export PATH=$PATH:$HOME/.local/bin && \
    echo export PATH=$PATH:\$HOME/.local/bin >> ~/.bashrc && \
    chmod a+x root/.local/bin/yle-dl && \
    rm -rf /var/lib/apt/lists/* 

WORKDIR /app

ENTRYPOINT ["/root/.local/bin/yle-dl"]

    
