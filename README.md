## Diet_Code:
This dir contains the implementation of [Diet Networks](https://arxiv.org/abs/1611.09340). The particular embedding we are going to use is the Histogram. The idea is to preprocess the data set by contructing a matrix s.t. each cell is the frequency of SNP k taking on value j for class i (where k is the SNP; j is 0,1,2; and i is 1,...,26). This is the embedding that is used for the auxilary networks which are used to construct the weight matrix in such a way that we greatly reduce the number of parameters. That is, we lean an embedding on the transpose of the data and construct a matrix that represents the first layer of the discrimative network (the net that makes predictions and optionally reconstructs using an autoencoder). 


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

