# OGC API in Switzerland
This repositoriy concerns the work done by HEIG-VD; SUPSI; and University of Geneva on the use of the new OGC APIs

## Installation PyGeoAPI
* docker pull geopython/pygeoapi
* docker create --name pygeoapi -p 5000:80 geopython/pygeoapi
* docker start|stop pygeoapi
* http://localhost:5000
* Documentation: https://docs.pygeoapi.io/

## Installation GeoServer with OGC API extension
* docker pull greggiuliani/gs_ogcapi
* docker create --name gs_ogcapi -p 8080:8080 greggiuliani/gs_ogcapi
* docker start|stop gs_ogcapi
* http://localhost:8080/geoserver
* Documentation: https://docs.geoserver.org/latest/en/user/community/ogc-api/index.html

> Connect in SSH: docker exec -it <your container name> /bin/bash

## Installation FROST with SensorThingsAPI
* wget https://raw.githubusercontent.com/FraunhoferIOSB/FROST-Server/master/scripts/docker-compose.yaml
* wget https://gist.githubusercontent.com/hylkevds/4ffba774fe0128305047b7bcbcd2672e/raw/demoEntities.json
* docker-compose up
* curl -X POST -H "Content-Type: application/json" -d @demoEntities.json http://localhost:8080/FROST-Server/v1.1/Things
* http://localhost:8080/FROST-Server/v1.0
* Documentation: https://fraunhoferiosb.github.io/FROST-Server/
