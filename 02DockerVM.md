# open a terminal & create a VOLUME
docker volume create 

# list the volumes
docker volume ls

# run a loginpage CONTAINER that will use the VOLUME
docker run -d --name voltest -v myvol:/app loginpage:latest

# connect to the instance(must be running CONTAINER)
docker exec -it -u="root" voltest /bin/sh #win shell
docker exec -it -u="root" voltest //bin/sh #git bash 

# run in the instance as root
docker run -it -u="root" loginpage /bin/sh

# install apps in container
apk update
apk -e search vim
apk info vim

# install nano or vim 
apk add vim

# create text file in vim
vim vimtest.txt

# type i for insert, "hello volume", :wq to save file
cat vimtest.txt

# type exit to quit instance
exit


