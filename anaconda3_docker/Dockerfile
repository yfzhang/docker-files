FROM continuumio/anaconda3
MAINTAINER yanfu <zhan0314@gmail.com>

# set up apt-get related tools
RUN apt-get update 
RUN apt-get install -y \
    curl \
    wget \
    vim \
    zsh \
    tree \
    git \
    cmake \
    htop \
    screen \
    man \
    lsof \
    openssh-server

# set up git
RUN git config --global user.email "zhan0314@gmail.com"
RUN git config --global user.name "yfzhang"
RUN git config --global credential.helper cache
RUN git config --global credential.helper 'cache --timeout=9999'

# set up conda env
RUN conda update -n base conda
RUN conda install tqdm
RUN conda install pytorch-cpu torchvision-cpu -c pytorch
RUN conda config --add channels conda-forge
#RUN conda install visdom
RUN conda update pip
RUN pip install visdom
RUN pip install git+https://github.com/daavoo/pyntcloud

# setup vim config and zsh config
RUN git clone --depth=1 https://github.com/amix/vimrc.git ~/.vim_runtime && \
    bash ~/.vim_runtime/install_awesome_vimrc.sh && \ 
    bash -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
