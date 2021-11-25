# MOLGENIS-EMX2 BIBBOX application

This container can be installed as [BIBBOX APP](http://bibbox.readthedocs.io/en/latest/admin-documentation/ "BIBBOX App Store") or standalone.
 
After the installation follow these [instructions](INSTALL-APP.md)

## Hints
* approx. time with medium fast internet connection: **15 minutes**
* initial user/password: **admin / admin**

## Standalone Installation

To install the app locally execute the commands:
* Clone the git repository: 
  * `sudo git clone https://github.com/bibbox/app-molgenis-emx2.git`
* change the current directory to app-molgenis: 
  * `cd app-molgenis-emx2/` 
* Change the permission of the directory `./data`: 
  * `chmod -R 777 data`
* Run **docker-compose up** in the root folder of the project: 
  * `docker-compose up -d`
 
After the installation (might take a few minutes) open **http://localhost:8080** in your browser to access Molgenis.
The default admin login is **user:admin/pw:admin**.

## Install within BIBBOX

Within BIBBOX you can use the [BIBBOX APP Store](http://bibbox.readthedocs.io/en/latest/admin-documentation/ "BIBBOX App Store") to install a lot of software tools. After the installation is finished you can start your application in the dashboard.

## Docker Images Used
 * [molgenis/molgenis-emx2](https://hub.docker.com/r/molgenis/molgenis-emx2), offical molgenis-frontend container 
 * [postgres:13-alpine](https://hub.docker.com/_/postgres), offical postgres container
 
## Mounted Volumes
* ./data/psql
