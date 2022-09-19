# Up Project in the server
## steps:
### 1. SSH Login into the server
### 2. Go to directory
    `/home/digitalprofile/work/kobo-docker`
### 3. Down all frontend container
    docker-compose -f docker-compose.frontend.yml -f docker-compose.frontend.override.yml -p kobofe down
### 4. Up all frontend container
    docker-compose -f docker-compose.frontend.yml -f docker-compose.frontend.override.yml -p kobofe up -d

#### Alternative Method
    use makefile :-
        make rweb 
    
#### Exceptions
    Sometimes restarting only frontend containers will not work.In this case start project again
    Note: you will not loose any server data and configs
    
    make start_project