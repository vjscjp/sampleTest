
## Releases
```
Releases - Manage releases (service deployment snapshots)

Commands available for Releases:
  Create  Deploy a project service build to an environment
  Get     Get a single release of a project
  GetAll  Get all releases for a project and environment
  Set     Set the default release for a service for use in subsequent commands.
```
##### Releases Create
```
Deploy a project service build to an environment
Usage: release create <project> <service> <environment> [<commitId>] [--latest] optionalArguments...
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
##### Releases Get
```
Get a single release of a project
Usage: release get <project> <environment> [<release>] [--latest] [--watch <timeout>]
  <project>         (required) Project for which to get releases
  <environment>     (required) Environment for which to get a release
  <release>         (optional) Release to get; if omitted, gets the release associated with the latest build
  --latest          (optional) Get the release associated with the latest build (overrides releaseId)
  --watch <timeout> (optional) Wait for build to deploy for a maximum of <timeout> minutes
Returns a release struct
```
##### Releases GetAll
```
Get all releases for a project and environment
Usage: release getall <project> <environment>
  <project>     (required) Project for which to get releases
  <environment> (required) Environment for which to get releases
Returns an array of Release structs
```
##### Releases Set
```
Set the default release for a service for use in subsequent commands.
Usage: release set <project> <service> <release>
  <project> (required) Project owning the release
  <service> (required) Service in the release
  <release> (required) Release to set as the default
Returns "OK" if successful
```
