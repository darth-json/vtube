# vtube


## Deployment 

The various V-Tube compoents are tied together using a `docker-compose.yml`. This defines a pod in docker-compose for running/deploying the entire v-tube application stack. In a perfect world I would configure an available Ci/Cd tool set to deploy my `develop` branch to a `development` set of containers, do some basic integration tests, and then auto-merge/release from `master` to production. For time's sake I will be manually managing my deployments to Docker-Hub and then to ECS. Note that while this is not my first time deploying into AWS and also not my first time using docker-compose, this will be my first time using ECS.

## Containers

Vtube is comprised of 3 main containers.

 - [VTube-UI]: The main ui for the application. Largely written in vue.js as a chance to use it some more. 
 - [VTube-Service]: The api-server for the V-Tube application.
 - [Mongo]: Configured and deployed in a non-clustered config for the sake of time. 


[Mongo]: https://hub.docker.com/_/mongo/
[VTube-UI]: https://github.com/darth-json/vtube-ui
[VTube-Service]: https://github.com/darth-json/vtube-service