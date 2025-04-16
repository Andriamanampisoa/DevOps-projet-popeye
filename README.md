# Popeye

The Popeye Project is a 1st year project at Epitech.\
This project aims to master the basics of containerizing applications and de-
scribing multi-containers infrastructures with Docker and Docker Compose. 

For this project, I needed to containerize and define the deployment of a simple web poll application.


### The Application

The application is composed of 5 elements:
- Poll, a Flask Python web application that gathers votes and push them into a Redis queue.
- A Redis queue, which holds the votes sent by the Poll application, awaiting for them to be consumed by the Worker.
- The Worker, a Java application which consumes the votes being in the Redis queue, and stores them into a PostgreSQL database.
- A PostgreSQL database, which (persistently) stores the votes stored by the Worker.
- Result, a Node.js web application that fetches the votes from the database and displays the result.

### The deployment
I had to create 3 images : Poll, Result and Worker.
Finally, I had to create a Docker Compose file which contains 5 services : Poll, Redis, Worker, Db and Result.



## Authors

- [@Toavina](https://github.com/Andriamanampisoa)
