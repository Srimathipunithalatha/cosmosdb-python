# Simple Python web backend with Cosmos DB and Fast API

This python project creates a very simple three-tiered ToDo web app backend using Cosmos DB as the database and FastAPI as the python web framework to expose API endpoints for performing CRUD operations.

## Features

This project demonstrates the use of the Cosmos DB python SDK with FastAPI . It covers the following aspects:

* Create Azure Cosmos DB Resource in Azure Portal 
* Setup the dev environment and install requisite client-side libraries
* Store Cosmos DB Resource connection credentials on our server 
* Connect to Cosmos DB Resource through python client 
* Define ToDoItem data model 
* Create the required database and container to store ToDo Items 
* Setup for API implementation 
* Write functions to interact with the database 
* Expose the API endpoints with FastAPI 
* Test the endpoints 

## Getting Started

### Prerequisites

- Python 3.6+

### Installation

Install the required libraries
- pip install fastapi
- pip install fastapi uvicorn
- pip install python-dotenv
- pip install aiohttp
- pip install azure-cosmos

### Quickstart

1. git clone [repository clone url]
2. cd [repository name]


## Demo

Test out the API endpoints:

1. cd [repository name]
2. uvicorn main:app –reload
3. In your browser, go to http://localhost:8000/docs 


## Resources

- Learn more about Azure Cosmos DB SQL API  - https://docs.microsoft.com/en-us/azure/cosmos-db/sql/




Python API app
Setup
Requirements:

Python (3.8+)
$ pip install -r requirements.txt
Or

$ poetry install
Running
Before running, set the .env by providing URI & Connection String of Cosmos DB.

Run the following common from the root of the api folder to start the app:

$ uvicorn main:app --port 3100 --reload
There is also a launch profile in VS Code for debugging.

Running in Docker
The environment variable AZURE_COSMOS_CONNECTION_STRING must be set and then application runs on TCP 8080:

docker build . -t imagename:version
docker run -p 3100:3100 -t imagename.version
Tests
The tests can be run from the command line, or the launch profile in VS Code

$ pip install -r requirements-test.txt
$ AZURE_COSMOS_DATABASE_NAME=test_db python -m pytest tests/
