# Local LLM (Large Language Model) Programming Environment

This project sets up a local environment for developing and testing an Large Language Model (LLM) using Docker Compose.

## Prerequisities

Installation of following utilities: 
- git
- docker with compose plugin (check following [link](https://docs.docker.com/compose/))
    - you can use Docker Desktop for Windows computer  

Open firewall for local port 11434.


## Local LLM setup

### Clone repository  
Use git to clone repository.  
`git clone https://github.com/devopsacid/local-llm.git`  


### Services

`ollama-webui`: A web-based interface for interacting with the LLM.  
`litellm`: A library for generating text based on input prompts. Uses Redis as a cache layer.  
`ollama`: The core LLM service, which uses NVIDIA GPU acceleration.  
`redis`: An in-memory data store used by litellm.


### Configuring

To configure this environment, you'll need to create the following files:

`data/ollama-webui`: A directory for storing webui-specific data.  
`config/litellm/config.yaml`: A configuration file for litellm. This is where you can customize parameters like port numbers and worker counts.
Running


### Start the environment

`docker-compose up -d`  

This will launch all services in detached mode.  
You can then access the webui at http://localhost:3002 and interact with the LLM using the litellm library via its API.

#### Download and run LLM model in ollama

Best local LLM models are LLaMa3.1 and Codestral for coding.  

Install both of them with `ollama` utility:  

`ollama run llama3.1`  
`ollama run codestral`


### Stopping

When you're finished, you can stop the environment with:

`docker-compose down`

## Setup your VScode properly
See following howto install [Visual Studio Code plugin](README-VScode.md).


Don't forget to change passwords to some local thing! 
-
May the force be with you!  
