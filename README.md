# Automatic Knative Service Manipulation

## Introduction

This is a VS Code extension which can help developers automatically deploying Knative services to the Kubernetes cluster. 

This extension is developed by Dongzhi Zhang and it's last updated on 2024/03/08.

## Prerequisites

Please ensure the following tools are set up in your local environment.

- Docker

- Kubernetes

- Knative

- Minikube

## Supported Commands

It currently supports the following commands:
 
 - **Deploy Service**: deploy the specified Knative service to Kubernetes (require inputs "register name" and "image name").

 - **Get Service Info**: print detailed information about the specified Knative service (require input "service name").
 
 - **Delete Service**: delete the specified Knative Service (require input "service name").
 
 - **Test Extension**: test whether the extension is working properly.

## Example Usage

1. Search for the extension "Automatic Knative Service Manipulation" in the marketplace and install it.

2. Open the folder containing the Flask app ready to run (the file should be named `app.py`). <u>Here I provide a folder called "quickstart", which contains a Flask app running a text classification ML task. You can conduct a brief test on the extension under the folder **(Ensure the root folder opened is "quickstart")**.</u>

3. In the VS Code palette (`Ctrl+Shift+P` or `Cmd+Shift+P` for Mac), execute `Test Extension` to test whether the extension is working properly.

4. To deploy the Knative service on the local Kubernetes for running the Flask app, execute `Deploy Service` in the VS Code palette. 

    - Enter the Docker image registry name.

    - Enter the desired Docker image name.

    - Now the deployment process will start. You can check the log terminal for latest progress.

    - After successfully deploying the Knative service, the service name will be printed in the log terminal.

5. To get the detailed information about the deployed Knative service, execute `Get Service Info` in the VS Code palette. You will need to enter the name of the Knative service.

6. Test whether the deployment succeeds.

    - `docker images` to check if the Docker image is successfully pushed. 

    - `kubectl get ksvc` to check if the Knative service is successfully deployed.

    - Check if the Flask app is running properly by testing its API with Postman.   

7. To delete a Knative service, execute `Delete Service` in the VS Code palette. The service to be deleted will be specified by the service name you then input in the palette.

## Relevant Tools

- Yeoman Generator
- Kubernetes
- Knative
- Docker
- Flask
- Hugging Face

## Release Notes

### 1.0.0

Initial release of "Automatic Manipulation on Knative Service". 

