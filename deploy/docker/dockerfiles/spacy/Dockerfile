ARG CUDA_VER='11.2.1'
ARG FLAVOUR='base' 
ARG DISTR='ubuntu20.04'

FROM nvidia/cuda:${CUDA_VER}-${FLAVOUR}-${DISTR}

ARG PYTHON_VER='3.8.8'

# install python build dependencies

ENV TZ=Europe/Moscow
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    git \
    rustc \
    cargo \
    make \
    build-essential \
    libssl-dev \
    zlib1g-dev \
    libbz2-dev \
    libreadline-dev \
    libsqlite3-dev \
    wget \
    curl \
    llvm \
    libncurses5-dev \
    xz-utils \
    tk-dev \
    libxml2-dev \
    libxmlsec1-dev \
    libffi-dev \
    liblzma-dev && \
    apt-get clean && \
    rm -rf /var/cache/apt/*

# install pyenv

RUN git clone https://github.com/pyenv/pyenv.git ~/.pyenv && \
    cd ~/.pyenv && \
    src/configure && \
    make -C src && \
    echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc && \
    echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc && \
    echo 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.bashrc

# install python
ENV HOME="/root"
WORKDIR $HOME
ENV PYENV_ROOT="$HOME/.pyenv"
ENV PATH="$PYENV_ROOT/shims:$PYENV_ROOT/bin:$PATH"

RUN pyenv install ${PYTHON_VER} && \
    pyenv global ${PYTHON_VER}

# install poetry

RUN curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python - && \
    echo 'export PATH="$HOME/.poetry/bin:$PATH"' >> ~/.bashrc

ENV PATH="$HOME/.poetry/bin:$PATH"
COPY pyproject.toml pyproject.toml
RUN poetry install

CMD ["poetry", "run", \
"jupyter-notebook", \
"--ip", "0.0.0.0", "--allow-root",\
"--NotebookApp.token=''", "--NotebookApp.password=''", "--no-browser", "/" ]

EXPOSE 8888