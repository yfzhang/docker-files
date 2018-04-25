# semantic_pytorch
FROM ubuntu:16.04
MAINTAINER yanfu <zhan0314@gmail.com>

RUN apt-get update 
RUN apt-get install -y \
    python3 \
    python3-pip \
    curl \
    wget \
    vim \
    zsh \
    tree \
    git \
    cmake \
    htop \
    screen \
    openssh-server

# setup vim config and zsh config
RUN git clone --depth=1 https://github.com/amix/vimrc.git ~/.vim_runtime && \
    bash ~/.vim_runtime/install_awesome_vimrc.sh && \ 
    bash -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
