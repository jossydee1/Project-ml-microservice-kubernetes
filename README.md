[![jossydee1](https://circleci.com/gh/jossydee1/project-ml-microservice-kubernetes.svg?style=svg)](https://app.circleci.com/pipelines/github/jossydee1/project-ml-microservice-kubernetes)

## Project Overview

In this project, i was tasked to apply the skills i have acquired in the Cloud DevOps Engineering course at Udacity to operationalize a Machine Learning Microservice API. 

I was given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. The data was initially taken from Kaggle, (https://www.kaggle.com/c/boston-housing). This project tests my ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

The goal of this project is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. 

In this project I performed the followig tasks:
* I tested my project code using linting
* I completed a Dockerfile to containerize this application
* I deployed my containerized application using Docker and made a prediction
* I improved the log statements in the source code for this application
* I configured Kubernetes and created a Kubernetes cluster
* I deployed a container using Kubernetes and made a prediction
* I uploaded a complete Github repo with CircleCI to indicate that my code has been tested

---

## Instructions as given by Udacity

## Setup the Environment

* Create a virtualenv with Python 3.7 and activate it. Refer to this link for help on specifying the Python version in the virtualenv. 
```bash
python3 -m pip install --user virtualenv
# You should have Python 3.7 available in your host. 
# Check the Python path using `which python3`
# Use a command similar to this one:
python3 -m virtualenv --python=<path-to-Python3.7> .devops
source .devops/bin/activate
```
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl


## A short explanation of the files in the repository

This repo contains several files that worked together to be able to actuallise the goal of this project which is to operationalize machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications.

The `config.yml` file is the file that makes the repo to communicate with circleci for project testing (check for error) to make sure the codes run and PASS without errors.

The docker_out.txt file contains the log info that was outputed after running `./run_docker.sh` on a terminal while prediction was made on another terminal.

The `kubernetes_out.txt` file contains the output after calling `run_kubernetes.sh` file. This file includes the pod’s name and status, as well as the port forwarding and handling text.

This repo contains other files like `Makefile`, `app.py`, `Dockerfile` and so on. Each of this files contribute to the accomplishment of the goal of this project. Hence, they are all important.