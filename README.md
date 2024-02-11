# Payoneer Counter Project

## Overview

Welcome to the Payoneer Counter Project! This project aims to provide a simple web service that maintains a counter of the amount of POST requests it serves.

## Project Structure

The project consists of a web service, "counter-service," written in Python, deployed using Docker, and managed by Jenkins for continuous integration and deployment.
It has webhook trigger for any branch,
Any branch other then 'main' will create a new docker deploy it wait 10 sec and close it.
In main branch changes it will delete the old counter-app and build the new container and deploy it.

Also you can Manually trigger the pipeline with branch name

## Getting Started

#  EVERYTHING SHOULD BE UP AND RUNNING BUT IF NOT:

1. Enter the vm

2. cd app

3. check if there is any docker running:
    ```sudo docker ps```

4. if not:
    ```docker-compose up -d```

5. Enter jenkins:
    http://ec2-3-120-148-111.eu-central-1.compute.amazonaws.com:443/
    user and pass sent by mail.
    check The job pipeline.

6. Access the counter service at http://ec2-3-120-148-111.eu-central-1.compute.amazonaws.com/.
   Also can curl post to increase and get to get the count
   ```curl -X POST http://ec2-3-120-148-111.eu-central-1.compute.amazonaws.com```
   ```curl -X GET http://ec2-3-120-148-111.eu-central-1.compute.amazonaws.com```

## Contact

For any inquiries or issues, please feel free to reach out to the project author:

- **Raz Leshem**
- **Phone:** 054-303-4383
- **Email:** razleshem3@gmail.com

Happy coding!