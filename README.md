# Bay Wheels and Lyft Bike Graph Analysis: Utilizing PySpark for Business Insights

The data used was provided by Bay Wheels (first regional and large-scale bicycle sharing system deployed in California) and can be found [here](https://www.lyft.com/bikes/bay-wheels/system-data). A more detailed project description can be found in my [portfolio](http://dylantbolt.com/lyft_bike). I leveraged software virtualization using docker to avoid downloading Spark on my local machine. Below are instructions for executing the notebook using Docker to avoid downloading Spark.

## Instuctions to Clone Repository

1. Cloning this repository will provide you with all the tools to recreate my analysis. Run this command to `clone` the repository:

```bash
git clone https://github.com/DylanBolt/lyft-bike_analysis.git
```

2. Change directory into this repository's directory:
```bash
cd lyft-bike_analysis
```

## Instructions for Docker Container Deployment

1. `pull` the jupyter/pyspark-notebook image using the following command:

```bash
docker pull jupyter/pyspark-notebook
```

2. Next, simply run the next command specifying an open port and file to mount to the container. The second part of the path is arbitrary and is used to navigate through the filesystem inside the container. 

```bash
 docker run -p {open port}:8888 -v  {file path leading to this cloned repo}:/home/jovyan/work jupyter/pyspark-notebook
 ```
 
 3. Navigate to http://localhost:{port assigned in previous step} to enter the container. Navigating to the "work" folder will show you all the necessary files such as the notebook and data.
 
