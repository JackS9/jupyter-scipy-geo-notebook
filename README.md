# jupyter-scipy-geo-notebook

This is the Dockerfile and requirements.txt file used to create jacks9/jupyter-scipy-geo-notebook on DockerHub

* The notebooks directory contains a sample notebook that will run in this environmentk.  
* The notebooks/data directory contains data files used by the notebook,

To rebuild the docker image:

'''
mkdir <my_docker_project>
cd <my_docker_project>
git clone https://github.com/jacks9/jupyer-scipy-geo-notebook.git .
docker build -t <your_hub_id>/jupyter-scipy-geo-notebook:<your_tag> .
'''

To run/test it:

'''
docker run -p 80:8888 -v $PWD:/home/jovyal/work <your_hub_id>/jupyter-scipy-geo-notebook:<your_tag>
'''

Then enter the URL displayed in your browser (using 'localhost' as the IP address).
