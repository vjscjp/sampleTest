## Configs
```
```
##### Configs Delete
```
```
##### Configs GetAll
```
```
##### Configs Set
```
```
##### Configs Update
```
```
## Configs
```
```
##### Configs Delete
```
```
##### Configs GetAll
```
```
##### Configs Set
```
```
##### Configs Update
```
```
## Configs
```
Configs - Show and modify config for service

Commands available for Configs:
  Delete  Delete a service configuration
  GetAll  Get all service configurations for a project, service, and environment
  Set     Set the default config ID
  Update  Update a project configuration
```
##### Configs Delete
```
Delete a service configuration
Usage: config delete <project> <service> <environment> <config>
  <project>     (required) Project with config to delete
  <service>     (required) Service with config to delete
  <environment> (required) Project environment with config to delete
  <config>      (required) Config to delete
Returns "OK" if successful
```
##### Configs GetAll
```
Get all service configurations for a project, service, and environment
Usage: config get <project> <service> <environment>
  <project>     (required) Project containing services to get
  <service>     (required) One of the project's services
  <environment> (required) One of the project's service environments
Returns an array of ServiceConfig structs
```
##### Configs Set
```
Set the default config ID
Usage: config set <config>
  <config> (required) Config to set as the default
Returns "OK" if successful
```
##### Configs Update
```
Update a project configuration
Usage: config update <project> <environment> <config> <optionalArgs>...
  <project>          (required) Project with config to update
  <service>          (required) Service with config to update
  <environment>      (required) Project environment with config to update
  <configID>         (required) ID of config to update
  ContainerCount=xxx (optional) The actual number of containers Marathon will deploy in this environment
  ContainerCPU=xxx   (optional) The actual CPU allocation marathon will use for deployments to this environment
  ContainerPort=xxx  (optional) The actual port marathon will use for deployments to this environment
  ContainerRAM=xxx   (optional) The actual RAM allocation marathon will use for deployments to this environment
  Deployimage=xxx    (optional) The image (usually found at registry.hub.docker.com) of the docker container in which to
                                run
Returns a ServiceConfig struct
```
