# formulador-back
## Introduction
## Getting Started
## Stack
## Understanding environments
## Understanding branches
- "master" branch is not used.
- "release" branch is the development branch.
- "hotfix" branch is for testing previous production deploy and fixing issues.
- The others branches are historic branches.
### Use of branches
- In the "release" branch we do the development planned, then we pass these changes to "hotfix" branch to testing and finally we do a promote to deploy to production.
- When using "hotfix" branch to fix an issue we must pull the these changes to "release" branch from "hotfix" branch.
## Running locally
### Requirements
- "db_dump_meal_labs" file, this file is a copy of database.
- Environment variables.
### Steps
1. Clone this repository
This project is in Docker.
- Open two terminals.
  * First terminal for run backend.
  * Second terminal for run database.
#### In first terminal:
2. Select one branch.  [Understanding branches](#understanding-branches)
3. Install Docker compose.
```
$ sudo apt install docker-compose
```
4. Add user to docker.
```
$ sudo usermod -aG docker $USER
$ su - $USER
```
5. Set the environment variables to .env file.
6. Run docker compose.
```
$ docker-compose up
```
- Here, two containers are generated.
  * database container, use postgres.
  * backend container, use debian os and django.
#### In second terminal:
7. Set local database.
- copy "db_dump_meal_labs" file into root project to load a copy of database.
8. Connect user to database.
```
$ sudo docker exec -it postgres sh
/ # psql -U meal_labs postgres
postgres=# exit
/ # exit
```
9. Reset current database into docker.
```
$ sudo docker exec -it postgres pg_dump -U meal_labs -c meal_labs_db
```
10. Copy the copy file of the database into docker.
```
$ sudo docker cp db_dump_meal_labs postgres:/tmp
$ sudo docker exec -it postgres psql -U meal_labs meal_labs_db -f /tmp/db_dump_meal_labs
```
Done!
### Use
Open your browser and run "localhost:8000".
### Login
- Username: VTCOL
- Password: v3rt1c4l_
##### Note:
In "devscripts" directory you can find:
- File named "enterapp" with a command to go into in the backend docker.
- File named "enterdb" with a command to go into in the database docker.
## Author
[Vertical Technologies](https://www.vertical.com.co)
---
## Suggestions
