# How to Install WordPress on Docker
This yaml file will start a MySQL DB container and a Wordpress container  
https://www.hostinger.com/tutorials/run-docker-wordpress#gref

- To run the file, make sure yaml file is in the same dir:
`docker-compose up -d`

- To visit the WP:
`http://IP:8000`

- To stop the containers:
`docker-compose down`

- To stop the containers and remove volme:
`docker-compose down -v`

- To check the volume
`docker volume ls`

