# semantic_pytorch
FROM nvidia/cuda:8.0-devel-ubuntu16.04
MAINTAINER yanfu <zhan0314@gmail.com>

RUN apt-get update && apt-get install -y --no-install-recommends apt-utils
RUN apt-get install -y build-essential
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
    libgtk2.0-dev \
    python3-tk \
    htop \
    screen \
    openssh-server
    
RUN pip3 install --upgrade pip && \
    pip3 install http://download.pytorch.org/whl/cu80/torch-0.3.0.post4-cp35-cp35m-linux_x86_64.whl \
    torchvision \
    visdom==0.1.4\
    colored-traceback \
    scikit-learn \
    pandas \
    scipy \
    ipython \
    tqdm \
    catkin-tools \
    Pillow \
    gym \
    opencv-python \
    matplotlib

# setup vim config and zsh config
RUN git clone --depth=1 https://github.com/amix/vimrc.git ~/.vim_runtime && \
    bash ~/.vim_runtime/install_awesome_vimrc.sh && \ 
    bash -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
