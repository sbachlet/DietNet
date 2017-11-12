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
- To save changes to Docker contain run: 
```
sudo docker commit <PID> <Instance Name>
```
