# create a VOLUME
docker volume create myvol

# inspect the volume
docker volume inspect myvol

# list the volumes
docker volume ls

# run a CONTAINER with a volume
docker run -d --name devtest -v myvol:/app loginpage:latest

# run a CONTAINER with a local folder
docker run -d --name devtest -v d:/test:/app loginpage:latest

# inspect the container
docker inspect devtest