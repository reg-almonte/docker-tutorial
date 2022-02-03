# Initial Code

## Initialize express-nodejs codes:
npx express-generator  
<br>

# Docker commands:

## Create docker network
docker network create mongo-network

## Start mongodb
 docker run -d \
 -p 27017:27017 \
 -e MONGO_INITDB_ROOT_USERNAME=admin \
 -e MONGO_INITDB_ROOT_PASSWORD=password \
 --network mongo-network mongo \
 --name mongodb \
 mongo



 ## Start mongo-express
 docker run -d 
 -p 8081:8081 \
 -e ME_CONFIG_OPTIONS_EDITORTHEME="ambiance" \
 -e ME_CONFIG_MONGODB_SERVER="mongodb" \
 -e ME_CONFIG_MONGODB_ADMINUSERNAME="admin" \
 -e ME_CONFIG_MONGODB_ADMINPASSWORD="password" \
 --network mongo-network \
 --name mongo-express \
 mongo-express


 These docker commands are translated to compose-docker.yaml