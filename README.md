ML MODEL SERVING WITH FASTAPI AND DOCKER

PROJECT OVERVIEW :
This project demonstrates end-to-end deployment of a machine learning model using FastAPI and Docker. It allows users to:
- Load a pre-trained scikit-learn model(pickled `.pkl` file).  
- Serve prediction endpoints via a REST API.  
- Containerize the API using Docker.  
- Test predictions with a Python client script or via Swagger UI.
  
KEY FEATURES :
- Pre-trained classification model served as an API.  
- JSON-based input for predictions.  
- Dockerized application for easy deployment.  
- Health-check endpoint included.  
- Example client script (`client.py`) provided for testing.

PROJECT STRUCTURE :
   ML-Model-Serving-with-FastAPI-and-Docker/
      ├── Dockerfile
      ├── requirements.txt
      ├── model.pkl
      ├── main.py
      ├── client.py
      └── README.md

- (Dockerfile)→ Instructions to build Docker image.  
- (requirements.txt)→ Python dependencies.  
- (model.pkl) → Pre-trained scikit-learn model.  
- (main.py) → FastAPI application.  
- (client.py) → Sample Python client to test the API.
  
PREREQUISITES :
- Docker installed  
  [Get Docker](https://www.docker.com/get-started)  
- Python 3.x installed (for client script)  
  [Get Python](https://www.python.org/downloads/)
  
Step 1: Clone the Repository
Open terminal or command prompt and run:
"git clone https://github.com/DuggireddyVarshini/ML-Model-Serving-with-FastAPI-and-Docker.git
cd ML-Model-Serving-with-FastAPI-and-Docker".

Step 2: Build the Docker Image
"docker build -t ml-fastapi-app" .

Step 3: Run the Docker Container
"docker run -p 8000:8000 ml-fastapi-app"
If successful, you’ll see:
"Uvicorn running on http://0.0.0.0:8000"

Step 4: Access API Documentation (Swagger UI)
Open your browser and go to:
http://localhost:8000/docs
Here you can:
-View all endpoints
-Send test requests
-Validate request and response formats
  
Step 5: Make Predictions Using Swagger
i)Click the /predict endpoint.
ii)Click “Try it out”.
iii)Enter JSON input (sample)
iv)Click Execute.
  Example response:
       {
          "prediction": 1,
          "label": "Malignant"
       }
       
Step 6: Test with Python Client
Ensure Python is installed.
Run the client script:
 "python client.py"
Output example:
     Status Code: 200
     {"prediction":1,"label":"Malignant"}


