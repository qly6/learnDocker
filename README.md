# learnDocker

# pull image
docker pull mong

# build image BE
docker build -t goals-node .

# build image FE
docker build -t goals-react .

# run container
mongo:docker run --name mongodb --rm -d -p 27016:27017 mongo
BE:docker run --name goals-be --rm -p 81:80 goals-node
FE:docker run --name goals-fe --rm -p 3000:3000 goals-react

# create network
docker network create goal-net
----------------
docker run --name mongodb --rm -d --network goal-net mongo
docker run --name goals-be --rm --network goal-net -p 81:80 goals-node
docker run --name goals-fe --rm -p 3000:3000 goals-react

# volume
docker run --name mongodb -v data:/data/db --rm -d --network goal-net mongo