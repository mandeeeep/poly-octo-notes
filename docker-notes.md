Docker Installation
.......
Docker Configuration

#### 1. Enabling docker

`systemctl enable docker`

#### 2. Starting docker

`systemctl start docker`

#### 3. Creating a mongo docker instance

`docker run --name dm36 -d mongo:3.6`
`docker run -p 27017:27017 -v /home/{user}/data:/data/db --name dm36 mongo:3.6`

#### 4. Delete all unused containers

`docker system prune`

#### 5. Removing docker containers

`sudo docker rm 60b9eb6a7d20`

#### 6. List Docker Containers

`docker ls -a`

#### 7. Remove docker images

`docker image rm 75835a67d134 2a4cca5ac898`

#### 8. Create mongodump from replica set
`mongodump --host "rs0/localhost:27017" --db DbName --excludeCollection=db.collec1 --excludeCollection=db.collec2 --excludeCollection=db.collec1 --excludeCollection=db.collec1 --excludeCollection=db.collec1 --gzip --archive=dump.gzip`
