# jupyter-scipy-geo-notebook

This is the Dockerfile and requirements.txt file used to create jacks9/jupyter-scipy-geo-notebook on DockerHub

* The notebooks directory contains a sample iPython notebook that will run in this Jupyter environment.  
* The notebooks/data directory contains data files used by the notebook.

To rebuild the docker image:
---

```
mkdir <my_docker_project>
cd <my_docker_project>
git clone https://github.com/jacks9/jupyter-scipy-geo-notebook.git
cd jupyter-scipy-geo-notebook
docker build -t <your_hub_id>/jupyter-scipy-geo-notebook:<your_tag> .
```

To run/test it:
---

```
docker run -p 80:8888 -v $PWD:/home/jovyan/work <your_hub_id>/jupyter-scipy-geo-notebook:<your_tag>
```

Then enter the URL displayed (including token) in your browser (using 'localhost' as the IP address).

You should see the notebook and data in the work directory.  

Open and run the notebook.

To just run the docker image as-is  on DockerHub
---
* Skip the docker build step 
* Use 'jacks9/jupyter-scipy-geo-notebook:latest' as the image name in the docker run step. 

You may still want to get the notebook and data from GitHub to test it. But you can skip that, too, and just upload or create your own notebook (and data).

To install Docker on your machine, go here:
---
https://docs.docker.com

To join DockerHub, go here:
---
https://hub.docker.com
