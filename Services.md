## Services
```
```
##### Services Check
```
```
##### Services Create
```
```
##### Services Delete
```
```
##### Services Get
```
```
##### Services GetAll
```
```
##### Services Repair
```
```
##### Services Set
```
```
##### Services Update
```
```
## Services
```
## Services
```
Services - Manage services (independently deployable components of a project)

Commands available for Services:
  Check   Check whether a project's services are ready for bootstrap - that is, that Shipped has successfully set up a
          GitHub repository and CI build for each service.
  Create  Create a service for a project
  Delete  Delete a project service
  Get     Get a project service or all of a project's services
  GetAll  Get all services for a project
  Repair  Repair a service that is not ready
  Set     Set service defaults on the Shipped console or in Shipped workflow
  Update  Update a service for a project
```
##### Services Check
```
Check whether a project's services are ready for bootstrap - that is, that Shipped has successfully set up a GitHub
repository and CI build for each service.
Usage: service check <project> [<service>]
  <project> (required) The project to check for bootstrap readiness
  <service> (optional) The service to check; if omitted, checks all services
Returns "OK" if successful
```
##### Services Create
```
Create a service for a project
Usage: service create <project> [<buildpack>|DeployImage=xxx] name=xxx <optionalArgs>...
If buildpackId is omitted, Shipped creates a service for a DockerHub image.
  <project>                    (required) The project for which to create the service
  <buildpack>                  (required) The buildpack to use for the service
  Name=xxx                     (required) The name of the service
  BootstrapTemplateRepo=xxx    (optional) The GitHub repository that hosts a sample hello-world implementation to use
                                          for a new service.
  BuildCommand=xxx             (optional) The shell command to build the service
  BuildImage=xxx               (optional) Build image used when building a service to be tested with Drone.
  ContainerPort=xxx            (optional) The application port used by Docker for this service
  ContainerSharedDirectory=xxx (optional) The location within the Docker container that will be shared with the host.
  CPU=xxx                      (optional) The number of CPUs required for the service
  Deployimage=xxx              (optional) The image (usually found at registry.hub.docker.com) of the docker container
                                          to use for the service
  EnvVariables=x:x             (optional) One or more environment variables to set in the service's container. Specify
                                          as a comma-separated list in the form env="name1:var1,name2:var2"
  ImageSource=xxx              (optional) A URL for an image used by this service
  Public=xxx                   (optional) Whether or not repository should be public (default true)
  RAM=xxx                      (optional) The amount of RAM required for the service
  Repository=xxx               (optional) The  GitHub repository for the service, in the form
                                          https://github.com/username/reponame (will be created if it doesn’t already
                                          exist)
  RunCommand=xxx               (optional) The shell command to run the service
  TestCommand=xxx              (optional) The shell command to run tests for the service
Returns a Service struct
```
##### Services Delete
```
Delete a project service
Usage: service delete <project> <service>
  <project> (required) The project for which to delete a service
  <service> (required) The service to delete
Returns "OK" if successful
```
##### Services Get
```
Get a project service or all of a project's services
Usage: service get <project> [<service>]
  <project> (required) The project for which to list service(s)
  <service> (optional) The service to list; if omitted, lists all services
Returns either a Service struct or an array of Service structs
```
##### Services GetAll
```
Get all services for a project
Usage: service getall <project>
Returns an array of Service structs
```
##### Services Repair
```
Repair a service that is not ready
Usage: service repair <project> <service>
  <project> (required) The project owning the service
  <service> (required) The service to repair
Returns OK if successful
```
##### Services Set
```
Set service defaults on the Shipped console or in Shipped workflow
Usage: service set <project> <service>
  <project> (required) The project owning the service
  <service> (required) The service to set as the default.
Returns the name of the service directory
```
##### Services Update
```
Update a service for a project
Usage: service update <project> <service> <optionalArgs...>
  <project>         (required) The project owning the service
  <service>         (required) The service to update
  BuildCommand=xxx  (optional) The shell command to build the service
  ContainerPort=xxx (optional) The container port used by Docker for this service
  DefaultRAM=xxx    (optional) The default RAM allocation for new environments for this service in Marathon
  ImageSource=xxx   (optional) The Docker image to use for the service
  Name=xxx          (optional) A new name for the service
  RunCommand=xxx    (optional) The run command used by docker for this service
  TestCommand=xxx   (optional) The shell command to run tests for the service
  EnvVariables=x:x  (optional) One or more environment varaibles to set in the service's container. Specify as a
                               comma-separated list in the form env="name1:var1,name2:var2". If specified, completely
                               replaces any existing environment variable specification.
Returns a Service struct
```
