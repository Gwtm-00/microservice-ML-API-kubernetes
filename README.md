[![CircleCI](https://circleci.com/gh/Gwtm-00/microservice-ML-API-kubernetes/tree/master.svg?style=svg)](https://app.circleci.com/pipelines/github/Gwtm-00/microservice-ML-API-kubernetes)

# Operationalize a Machine Learning Microservice API

### Project Overview
A pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on the data source site. This project tests your ability to operationalize a Python flask app—in a provided file, app.py—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Environment Setup
* Create a virtual environment 
`python3 -m venv ~/.devops`
* Activate it
`source ~/.devops/bin/activate`

### Kuberneted Environment setup
* Install minkube
* `minikube start`

### Running Script
* Start server : `python app.py`
* Run in Docker: `./run_docker.sh`
* Run in Kubernetes: `./run_kubernetes.sh`


### Files

* `app.py` ---> contains app logic and flask module
* `requirements.txt` ---> contains list of third-party libraries and framework used
* `run_docker.sh` ---> builds docker image 
* `upload_docker.sh` ---> Uploads docker image to docker hub
* `run_kubernetes.sh` ---> runs the container in kubernetes cluster
* `Makefile` ---> Takes care of installing dependencies and linting
* `make_prediction.sh` ---> forwards input to the running server
* `.circleci` ---> contains config file for circel CI


