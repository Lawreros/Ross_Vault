Installation:
- Get image from here: https://github.com/pytorch/pytorch#docker-image

Getting the error message: `Could not select device driver "" with capabilities: [[gpu]]`
- Means that you haven't set up the gpu connections properly. To fix this install `Nvidia Container Toolkit` https://github.com/NVIDIA/nvidia-container-toolkit
	- Follow the steps here: https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html
- Test that everything worked by running the following: 
``` bash
docker run --gpus all -it pytorch/pytorch:latest /bin/bash 
```

- Create a directory with the proper mounted files
```bash
docker run --gpus all --shm-size 3G -it --name retinanet --mount type=bind,source=/home/ross/Documents/CODE/RetinaNet,target=/workspace pytorch/pytorch:latest /bin/bash
```
`pip install pycocotools scikit-image`
