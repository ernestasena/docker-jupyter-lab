FROM python:3.8.5-slim 

USER root

COPY . .

RUN apt-get update --fix-missing && apt-get install -y \
    libpq-dev \
    python-dev \
    python3-dev \
    python3-pip \
    python3-llvmlite \
    build-essential \
    && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
    
RUN pip install jupyterlab
RUN pip install pandas
RUN pip install sklearn
RUN pip install numpy
RUN pip install SQLAlchemy
RUN pip install seaborn
RUN pip install matplotlib

WORKDIR /home/jovyan/

# COPY ./requirements.txt /home/jovyan/requirements.txt
# RUN pip --no-cache-dir install -U -r /home/jovyan/requirements.txt
