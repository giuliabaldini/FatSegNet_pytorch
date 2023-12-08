FROM nvcr.io/nvidia/pytorch:20.01-py3

# install dependencies from python packages
RUN pip install --upgrade pip \
    && pip3 install nibabel==2.5.1 numpy==1.17.4 scipy==1.3.1 scikit-image==0.15.0 pandas==0.21.0 matplotlib==3.0.3

## Clone FatSegnet Code from repository
RUN mkdir /FatSegNet
RUN git clone https://github.com/reuter-lab/FatSegNet_pytorch.git /FatSegNet

WORKDIR "/FatSegNet/fatsegnet"

ENTRYPOINT ["python3","./run_fatsegnet.py"]
