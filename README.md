## Data Science Docker:
This repo is a fork of ljstrnadiii/DietNet and is used as a base for running Tensor Flow GPU on googles cloud computing paltform.

#### Setup:

- Build environment image:
```
sudo docker build -t diet_code_env -f Dockerfile.gpu .
```
- Launch the container and place add the volume with the data we are using:
```
sudo nvidia-docker run -it -p 81:6006 diet_code_env
```
- Setup git info:
```
git config --global user.name "Your Name"
git config --global user.email "your.email@website.com"
```
- Unzip training and test data:
```
cd /usr/local/DataScience5800/Keras
unzip "en_test.csv (2).zip"
unzip "en_train.csv (2).zip"
```
- Save the state of you instance:
```
ctrl-p ctrl-q
sudo docker commit <PID> diet_code_env
sudo docker ps
sudo docker exec -it <PID> /bin/bash
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
### Tensor Board Commands
- To start Tensorboard
```
tensorboard --logdir/logs
```
- To view graph:
```
http://localhost:6060
```
