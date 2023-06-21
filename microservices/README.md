# Microservices
## 
This folder contains 4 microservices utilized in the master's dissertation "Data-based compliance checking against building requirements". They are developed to illustrate the capabilities of microservices in conjuction with BPMN diagrams. They can be coupled to the the illustrative example provided in the Proof of Concept Application at https://github.com/simonbaecke/masters-dissertation-poc, but can also be used independently.
## Installation
To install a microservices, make sure Python 3.9 or higher is installed on your device. Each folder contains one microservice, so the operations have to be performed on the folder of the desired microservice. Installing the microservice can be done by first starting a Python virtual environment and then installing the dependencies stored in the pyproject.toml file. The virtual environment is activated using the following commands.
```
python -m venv .venv
.venv\Scripts\activate
```
The microservice and its dependencies can now be installed using the following command.
```
pip install -e .
```
## Running the microservice
To run the microservice, a virtual environment needs to be activated using the following command.
```
.venv\Scripts\activate
```
After the virtual environment is activated the microservice can be run using the following command. Additional arguments can be added to the command to for example run the microservice in debug mode (--debug), which enables live reloading. The port on which the microservice runs can also be changed with an additional argument (--port <port-number>).
```
flask --app flaskr run
```
## Dockerizing a microservice
To Dockerize a microservice, make sure Docker is installed. The Microservice can be built into a Docker Image using the following command.
```
docker build -t <image-name> .
```
To run the Docker image in a Docker Container, use the following command.
```
docker run <image-name>
```

## Reference
The microservice designs are based on the proposal of Lemmens (2023) to implement a microservice architecture in the AEC domain. The template can be found at https://github.com/stelemme/template-microservice-py.