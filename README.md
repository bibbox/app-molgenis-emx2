# molgenis-emx2 BIBBOX application

This container can be installed as [BIBBOX APP](https://bibbox.readthedocs.io/en/latest/ "BIBBOX App Store") or standalone. 

- after the docker installation follow these [instructions](INSTALL-APP.md)

## Standalone Installation 

Clone the github repository. If necessary change the ports in the environment file `.env` and the volume mounts in `docker-compose.yml`.

```
git clone https://github.com/bibbox/app-molgenis-emx2
cd app-molgenis-emx2
docker-compose up -d
```

The main app can be opened and set up at
```
http://localhost:8080
```

## Install within BIBBOX

Visit the BIBBOX page and find the App by its name in the Store. Click on the symbol and select Install. Then fill the parameters below and name your app click install again.

## Docker Images used
  - [postgres](https://hub.docker.com/r/postgres) 
  - [molgenis/molgenis-emx2](https://hub.docker.com/r/molgenis/molgenis-emx2) 
  - [molgenis/ssr-catalogue](https://hub.docker.com/r/molgenis/ssr-catalogue) 


 
## Install Environment Variables
  - DB_PASSWORD = Database password, please change for production

  
The default values for the standalone installation are:
  - DB_PASSWORD = changethispasswordinproductionenvironments

  
## Mounted Volumes
### postgres Conatiner
  - *./data/psql:/var/lib/postgresql/data*
  - *./data/initdb.sql:/docker-entrypoint-initdb.d/initdb.sql*
