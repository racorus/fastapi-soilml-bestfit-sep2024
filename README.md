####### This Model has trained from 629 Sample data with | sand/silt/clay #############

## Model Trained joblib file using ##
scikit-learn==1.2.2
#####################################

# FastAPI App template

___

## Prequisitions

- Docker and Docker Compose

## Pre-Installation

1. Update required python packages in <code>requirements.txt</code>
2. Update expose port of FastAPI app in <code>docker-compose.yml</code> under <code>ports</code> to be <code>{expose_port}:80</code>
3. Copy model file to <code>./model/</code> directory
4. Copy samples training data to <code>./data/</code> directory

## Installation
1. <code>cd</code> to project directory
2. run command <code>docker-compose up -d --build</code>
3. check Web UI at <code>{IP:port}</code> as defined

## Clean
docker system prune -a

## Rebuild
docker-compose up -d --build

## Test the Prediction Endpoint
Send a request to the /predict endpoint with the required query parameters:
http://localhost:80/predict?soil_type=clay&temp=25.0&humid=40.0&ph=6.5&n=10.0&p=15.0&k=20.0&ec=1.0
https://localhost:80/predict?soiltype=sand&test_temp=27.3&test_humid=60.7&test_PH=3.9&test_N=0&test_P=44&Test_K=36&test_Conductivity=180

