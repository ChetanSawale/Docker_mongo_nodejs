## Docker Practice — EC2 + MongoDB Container

This project was used to practice deploying and containerizing a Node.js application on an AWS EC2 instance.

### What I Practiced

- Set up a Node.js + Express application on EC2
- Configured application environment variables
- Ran MongoDB 7 using Docker
- Configured Docker port mapping (`27017:27017`)
- Connected the Node.js application to MongoDB running in Docker
- Tested the REST API using Postman
- Verified stored data directly inside the MongoDB container
- Troubleshot Docker disk-space issues
- Troubleshot MongoDB version and Linux kernel compatibility

### Current Architecture

```text
AWS EC2
│
├── Node.js + Express API
│       │
│       │ localhost:27017
│       ↓
└── MongoDB Docker Container


# Docker Practice — Node.js + MongoDB on AWS EC2

This project is a hands-on Docker practice project where I containerized a Node.js/Express e-commerce API and MongoDB and connected them using a Docker network.

The project was deployed and tested on an AWS EC2 instance.

## Architecture

```text
                    AWS EC2
                       |
              +--------+--------+
              |                 |
         Node.js API        MongoDB
         Container          Container
          :5000              :27017
              |                 |
              +-------+---------+
                      |
                Docker Network
                  my-network
                      |
                mongodb-data
                 Docker Volume
