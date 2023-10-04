# molgenis-emx2 BIBBOX application

This container can be installed as [BIBBOX APP](https://bibbox.readthedocs.io/en/latest/ "BIBBOX App Store") or standalone. 

After the docker installation follow these [instructions](INSTALL-APP.md).

Initial User/Password: admin/admin

## Standalone Installation 

Clone the github repository. If necessary change the ports in the environment file `.env` and the volume mounts in `docker-compose.yml`.

```
git clone https://github.com/bibbox/app-molgenis-emx2
cd app-molgenis-emx2
chmod -R 777 data
docker network create bibbox-default-network
docker-compose up -d
```

The main App can be opened and set up at:
```
http://localhost:8080
```

## Install within BIBBOX

Visit the BIBBOX page and find the App by its name in the store. Click on the symbol and select install. Then fill the parameters below and name your App, click install again.

## Docker Images used
  - [postgres](https://hub.docker.com/r/postgres) 
  - [molgenis/molgenis-emx2](https://hub.docker.com/r/molgenis/molgenis-emx2) 
  - [molgenis/ssr-catalogue](https://hub.docker.com/r/molgenis/ssr-catalogue) 


 
## Install Environment Variables
  - DB_PASSWORD = Database password, please change for production

  
The default values for the standalone installation are:
  - DB_PASSWORD = changethispasswordinproductionenvironments

  
## Mounted Volumes
### postgres Container
  - *./data/psql:/var/lib/postgresql/data*
  - *./data/initdb.sql:/docker-entrypoint-initdb.d/initdb.sql*

