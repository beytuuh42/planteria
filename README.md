# Planteria

A WIP full-stack web application for tracking the irrigation of plants.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)

## Installation
### Docker
Run ```docker compose up```. This will create 4 containers: frontend (Angular), backend (Django), database (Postgre) and DBMS (PGAdmin).

### Alternative
The other option is to install the packages manually by running  ```pip install - requirements.txt``` in the backend folder and first ```npm install -g @angular/cli@15.2.9``` to install Angular globally and afterwards ```npm i``` in the frontend folder to install all frontend packages. These commands will install all necessarry packages to run the projects. PGAdmin4 needs to be downloaded and installed separately, or any other database client software that works with PostgreSQL.

## Usage
### Docker
The Docker command will download the images for the containers, install all necessary packages and serve all applications on host:port defined in the .env file, which should be changed. The frontend and backend have their own Dockerfiles for additional configuration. 

### Alternative
I recommend using Docker because by running a single command everything is aligned to run in sync. Otherwise, all environment variables have to be re-configured, from the command line, when running the applications and in the project files.

#### Backend
In the backend folder run after the installation ```python manage.py makemigrations```, which will generate SQL commands to be executed with ```python manage.py migrate```. Afterwards run ```python manage.py runserver```.

#### Frontend
Just run ```ng serve```.