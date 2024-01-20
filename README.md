# learnDocker

# pull image
docker pull mong

# run Container 
docker run --name mongodb --rm -d -p 27016:27017 mongo

# build image BE
docker build -t goals-node .

# build image FE
docker build -t goals-react .

# run container
BE:docker run --name goals-be --rm -p 81:80 goals-node
FE:docker run --name goals-fe --rm -p 3000:3000 goals-react