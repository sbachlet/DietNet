## Data Science Docker:
This repo is a fork of ljstrnadiii/DietNet and is used as a base for running Tensor Flow GPU on googles cloud computing paltform.

#### Preprocess:

- Build environment image:
```
sudo docker build -t diet_code_env -f Dockerfile.gpu .
```
- launch the container and place add the volume with the data we are using:
```
sudo nvidia-docker run -it -p 81:6006 -v /path/to/4files:/usr/local/diet_code/1000G diet_code_env
```

### Docker Commands

- To list running instances:
``` 
sudo docker ps
```
- To start a Docker instance:
```
sudo nvidia-docker run -it -p 81:6006 diet_code_env
```
- To kill a Docker instance from inside instance:
```
ctrl-d 
```
- To kill a Docker instance from outside instance: 
```
sudo docker kill <PID>
```
- To exit a Docker instance:
```
ctrl-p ctrl-q
```
- To re-enter a Docker instance 
```
sudo docker exec -it <PID> /bin/bash
```
- To save changes to Docker contain run: 
```
sudo docker commit <PID> <Instance Name>
```
