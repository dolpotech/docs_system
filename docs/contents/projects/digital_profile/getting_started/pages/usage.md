##Docker Operations
###To run containers:
1. Go inside the kobo-docker folder to run these scripts.
2. First run backend containers using code
   
    ```
    sudo docker-compose -f docker-compose.backend.primary.yml -f docker-compose.backend.primary.override.yml -p kobobe up -d
    ```
   

3. Secondly, run frontend containers using code
   
   ```
   sudo docker-compose -f docker-compose.frontend.yml -f docker-compose.frontend.override.yml -p kobofe up -d
   ```

   
###To stop containers
1. Go inside the kobo-docker folder to run these scripts.
2. First stop frontend containers

```
sudo docker-compose -f docker-compose.frontend.yml -f docker-compose.frontend.override.yml -p kobofe down

```

3. Secondly, stop backend containers

```
sudo docker-compose -f docker-compose.backend.primary.yml -f docker-compose.backend.primary.override.yml -p kobobe down
```
Note: you can also use makefile for these commands

## BACKUPS

## taking backup from vps
1. go to vps root@207.180.193.75 (bmis_kobo/bmis folder)
2. take koboforms backup: docker exec  -t kobobe_postgres_1 pg_dump -c -U kobo kobocat > kobocat_5.sql
3. take kobocat backup: docker exec  -t kobobe_postgres_1 pg_dump -c -U kobo koboform > koboform_5.sql

## copying backups from remote to local
** run this in bmis dir **
for koboform
1.mkdir backups (in bmis dir--make sure to keep in gitignore)
1.rsync -avzP root@207.180.193.75:bmis_kobo/bmis/backups/kobocat_5.sql /backups
for kobocat
2.rsync -avzP root@207.180.193.75:bmis_kobo/bmis/backups/kobocat_5.sql /backups

   
##Database Backup
###steps
1. Make sure all kobofe containers are down
2. Go into `kobobe_postgres_1` container
   
   `docker exec -it kobobe_postgres_1 bash`
   

3. log in as kobo user
   
   `psql -U kobo`
   

4. Delete `kobocat` database
   
   `drop database kobocat;`
   

5. Delete `koboform` database
   
   `drop database koboform;`
   

6. Create new `koboform` database

   `create database koboform`;

7. Create new kobocat database
   
    `create database kobocat;`
   
**import database**

After the above steps have been completed, follow the below steps to import database
1. Go to the folder where sql files are located
   
2. To import koboform database
   
	```
    cat koboform_18-05-2021_09_21_52.sql | sudo docker exec -i kobobe_postgres_1 psql -U kobo -d koboform
   

3. To import kobocat database
   
	```
    cat kobocat_1.sql | sudo docker exec -i kobobe_postgres_1 psql -U kobo -d kobocat
 
   
4.Down all the kobofe and kobobe containers and start them again. Now the data in server has been imported in your local machine.
   
5. Username and password is also changed as per server's admin credentials.


## Taking Media Backups
media file is already in our project root at kobcat_media folder
1. go to kobofe_bmis_1 container
    make bweb
2. go to kobocat_media
    cd kobocat_media/super_admin
3. remove attachments
    rm -r attachments
4. copy kobocat_media file to kobofe_bmis_1 container(Run this command in bmis directory)
    docker cp kobocat_media/super_admin/attachments/ kobofe_bmis_1:code/kobocat_media/super_admin/



## Commands
To use this project, run this commands at  project dir:

0. `make df`
   
   to down the frontend containers
1. `make db`
   
    to down the backend containers
2. `make dd` 
    
    to down both frontend and backend containers
3. `make uf` 
    
    to up frontend containers
4. `make ub`
    
    to up backend containers
5. `make du` 
    
    to  up backend and frontend containers
6. `make bweb`
    
    to shell access web container (kobofe_bmis_1).
7. `make cs`
    
    to put static files in static directory.
8. `make nrw`
    
    to run npm run watch.
9. `make nrp` 
   
    to run npm run production.
10. `make l` 
    
    to log access all kobo containers.
11. `make stop` 
    
    to stop kobo containers (by python3 run.py).
12. `make dr` 
    
    to restart web container.
13. `make setup` 
    
    to run new kobo setup .
14. `make mm` 
    
    to make migrations
15. `make m` 
    
    to migrate
16. `make idr` 
    
    to install dev requirements
17. `make iar` 
    
    to install apt requirements
18. `make dr1` 
    
    to down frontend container and access postgres db shell

##ps. you can explore more in Makefile
