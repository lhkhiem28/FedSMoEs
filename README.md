
Currently installed versions:

``bash
python -c  'import torch; print(torch.__version__); print(torch.cuda.nccl.version())'
``
> 2.4.0                                                                                                 
(2, 20, 5)  



## Install Requirements
```bash
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2204/x86_64/cuda-keyring_1.0-1_all.deb
sudo dpkg -i cuda-keyring_1.0-1_all.deb
sudo apt-get update
sudo apt install libnccl2 libnccl-dev
conda install pytorch torchvision torchaudio pytorch-cuda=12.4 -c pytorch -c nvidia
```
## Download dataset

```bash
mkdir -p data/enwik8
wget https://mattmahoney.net/dc/enwik8.zip
wget --continue http://mattmahoney.net/dc/enwik8.zip
wget https://raw.githubusercontent.com/salesforce/awd-lstm-lm/master/data/enwik8/prep_enwik8.py
python3 prep_enwik8.py
