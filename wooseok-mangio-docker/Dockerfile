FROM nvidia/cuda:11.8.0-cudnn8-runtime-ubuntu22.04
# FROM nvidia/cuda:12.0.1-cudnn8-runtime-ubuntu22.04

RUN apt-get update \
        && apt-get install -y python3.10 python3-pip git\
        && apt-get clean \
        && rm -rf /var/lib/apt/lists/*


WORKDIR /

COPY Mangio-RVC-Fork/requirements.txt .

RUN python3.10 -m pip install -r requirements.txt
RUN rm requirements.txt

RUN python3.10 -m pip install ffmpy soundfile -U

WORKDIR /app