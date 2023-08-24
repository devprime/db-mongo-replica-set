# MongoDB
Transaction demonstration with a database requires the utilization of the MongoDB replica set. In this example using Docker Compose, it's possible to recreate an environment for local testing.

Requirements:
- An updated version of Docker

Follow the guide:

1) Modify the etc\hosts file on Windows / Linux / Mac.

a) In the Windows environment, you'll find a directory similar to "C:\Windows\System32\drivers\etc\hosts".

b) Add the following entries to the etc\hosts file.

127.0.0.1 mongo1
127.0.0.1 mongo2
127.0.0.1 mongo3

2) Run the Docker Compose in the directory:
docker-compose up -d

3) To connect using MongoDB Compass:
a) Use the connection string

mongodb://mongo1:30001,mongo2:30002,mongo3:30003/?replicaSet=my-replica-set&tls=false