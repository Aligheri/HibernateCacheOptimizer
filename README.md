How to Run the Project

Step 1: Set up MySQL Server as a Docker Container
To run the MySQL server as a Docker container, execute the following command:

Copy code:

	docker run --name mysql -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD=root --restart unless-stopped -v mysql:/var/lib/mysql mysql:8


Step 2: Deploy the Database Dump
Download the database dump from the repository and deploy it.

Step 3: Launch Redis Server as a Docker Container
Run the following command to start the Redis server as a Docker container:


Copy code:

	docker run -d --name redis -p 6379:6379 redis:latest
Project Overview

In this project, the following functionalities have been implemented:

Retrieve Data from MySQL:
Implement a method to fetch all data from the MySQL database.

Data Transformation:
Implement a method to transform data (only data frequently requested is stored in Redis).

Write Data to Redis:
Develop functionality to write data to Redis.

Retrieve Data from Redis:
Implement a method to retrieve data from Redis.

Retrieve Data from MySQL (again):
Develop a method to fetch data from MySQL.

Benchmarking:
Compare the speed of retrieving the same data from MySQL and Redis.

Note: Ensure that both MySQL and Redis containers are running before executing any functionality in the project.

If you encounter any issues or have suggestions, please open an issue on GitHub.
