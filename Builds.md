
## Builds
```
Builds - Build status and logs for service

Commands available for Builds:
  Deploy   Deploy a project service build to an environment
  Get      Get project builds for a single service or for all services
  GetLogs  Get the logs for a service build
  Set      Set the default build and commitID for a service.
```
##### Builds Deploy
```
Deploy a project service build to an environment
Usage: build deploy <project> <service> <environment> [<commitId>] [--latest] optionalArguments...
  <project>                  (required) The project owing the service that was built
  <service>                  (required) The service owning the build
  <environment>              (required) The environment where the build should be released
  <commitId>                 (optional) The commitID of the build to release (defaults to latest build if omitted)
  --latest                   (optional) Select latest build (overrides commitId)
  ConfigID=xxx               (optional) ConfigID to be deployed.
  ContainerCount=xxx         (optional) Number of service Docker containers to deploy
  ContainerCPU=xxx           (optional) Number of vCPUs to allocate per container.
  ContainerPort=xxx          (optional) Port used to access app inside the container and that should be exposed outside
                                        the container.
  ContainerRAM=xxx           (optional) RAM in MB to be allocated for container
  DeployedURL=xxx            (optional) Where the service is or would be running
  DeployImage=xxx            (optional) The Docker image deployed.
  DeploymentId=xxx           (optional) The Docker image that got deployed.
  EnvVariables=xxx           (optional) Set additional configuration variables. These are set as env variable on Docker
                                        instances.
  ErrorMsg=xxx               (optional) Populated if there was a problem
  HealthCheckMaxFailures=xxx (optional) Health check failure before marking service as down, default by buildpack.
  HealthCheckPath=xxx        (optional) Health check endpoint URL, default by buildpack.
  HealthCheckProtocol=xxx    (optional) Health check protocol, default by buildpack.
  MarathonAppID=xxx          (optional) The marathon identifier for the app
  RepoURL=xxx                (optional) The GitHub repo for the app
  ServiceType=xxx            (optional) App, RepoApp, or Service
  SnapshotID=xxx             (optional) If multiple services are deployed from a single deploy, they all have the same
                                        snapshotID. Useful for rollbacks
Returns a Release struct
```
##### Builds Get
```
Get project builds for a single service or for all services
Usage: build get <project> [<service>] [--latest] [--logs] [--watch <timeout>]
  <project>         (required) Project for which to get builds
  <service>         (optional) Sservice for which to get builds; if omitted, gets builds for all services
  --latest          (optional) Retrieve only the latest (most recent) build
  --logs            (optional) Show logs from build if available
  --watch <timeout> (optional) Wait for build to complete for a maximum of <timeout> minutes
Returns an array of build structs
```
##### Builds GetLogs
```
Get the logs for a service build
Usage: build getlogs <project> <service> [<build>] [--latest]
  <project>           (required)                                                       Project with service for which
                                                                                       build logs are desired
  <service>           (required)                                                       Service for which build logs are
                                                                                       desired
  <build> (optional)  Build for which logs are desired (defaults to latest if omitted)
  --latest (optional) Get logs for latest build (overrides buildId)
Returns logs for one of a project's service builds
```
##### Builds Set
```
Set the default build and commitID for a service.
Usage: build set <project> <service> [<build>] [--latest]
  <project> (required) Project owning the build
  <service> (required) Service built by the build
  <build>   (optional) Build to set as the default.
  --latest  (optional) Set build to that of the most recent build (and ignore the <build> argument)
Returns "OK" if successful
```
