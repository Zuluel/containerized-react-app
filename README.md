This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Docker React App 

### Getting Started 
> Requirements:
  - Docker
  - NPM
  
**Setting Up**
> Clone the repo
    
    git clone https://github.com/Zuluel/containerized-react-app.git
    
##### Development Environment:
    
> Install dependencies and run the container using dockerfile, run the command:

    1. docker build -f Dockerfile.dev -t sample:dev
    2. docker run -it --rm -v ${PWD}:/app -v /app/node_modules -p 3000:3000 -e CHOKIDAR_USEPOLLING=true sample:dev

> OR, install dependencies and run the Container using docker-compose, run the command:
 
    1. docker-compose up
    
    
> note: you may replace sample:dev to any naming convention you may like.
    
> Open your browser and go to [localhost:3000](http://localhost:3000)

##### Production Environment:

> Using Dockerfile to build and spin up the production server

    1. docker build -f Dockerfile -t sample:prod .
    2. docker run -it --rm -p 1337:80 sample:prod
    
> Using Docker-compose to build and spin up the production server

    1. docker-compose -f docker-compose.prod.yml up -d --build


> note: you may replace sample:prod to any naming convention you may like.
    
> Open your browser and go to [localhost:1337](http://localhost:1337)
