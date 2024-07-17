# open a terminal & create a VOLUME
docker volume create 

# list the volumes
docker volume ls

# run a loginpage CONTAINER that will use the VOLUME
docker run -d --name voltest -v myvol:/app loginpage:latest

# connect to the instance
docker exec -it voltest /bin/sh

# run in the instance as root
docker run -it -u="root" loginpage /bin/sh
