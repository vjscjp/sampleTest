## Local
```
```
##### Local Bootstrap
```
```
##### Local Ports
```
```
##### Local Commit
```
```
##### Local Destroy
```
```
##### Local Logs
```
```
##### Local Reload
```
```
##### Local Status
```
```
##### Local Start
```
```
## Local
```
```
##### Local Bootstrap
```
```
##### Local Ports
```
```
##### Local Commit
```
```
##### Local Destroy
```
```
##### Local Logs
```
```
##### Local Reload
```
```
##### Local Status
```
```
##### Local Start
```
```
## Local
```
Local - Local [desktop] development environment management
----------------------------------------------------------
Each service in a project runs in its own Docker container, with the containers hosted in a Docker host VM. A service's
local source repository is shared with its container, so that changes you make on your desktop are available to the
container.  You build, run, and test your code in the container, while maintaining it on your desktop.


Commands available for Local:
  Bootstrap  Bootstrap a Shipped project
  Commit     Commit changes to a Shipped project and start a CI build.
  Destroy    Destroys containers running project services.  Use lcl bootstrap to recreate.
  Logs       Show log files that a service has written to its container.
  Ports      Show information about ports used by Shipped
  Reload     Halts and restarts project containers
  Start      Start all of a project's services
  Status     Shows the status of the project's VM and its service containers.
```
##### Local Bootstrap
```
Bootstrap a Shipped project
Usage: lcl bootstrap <project> [--fast]
  <project> (required) Project to bootstrap
  --fast    (optional) Speed up bootstrap by skipping VM and container deployment
Returns the bootstrap log
```
##### Local Ports
```
Show information about ports used by Shipped
Usage: lcl ports [<subcommand>]
  ports global-list - list all ports in use on this machine
  ports list        - (default) list ports in use for current user and API server
  ports release n1[, n2...] - release one or more ports
```
##### Local Commit
```
Commit changes to a Shipped project and start a CI build.
Usage: lcl commit <project> [<service>] message=xxx
  <project>   (required) Project to commit
  <service>   (optional) Service to commit; if omitted, commits all services
  message=xxx (required) Commit message
Returns Git output
```
##### Local Destroy
```
Destroys containers running project services.  Use lcl bootstrap to recreate.
Usage: lcl destroy <project> [<service>]
  <project> (required) Project for which to destroy service containers
  <service> (optional) Service for which to destroy the container; if omitted, destroys all service containers
```
##### Local Logs
```
Show log files that a service has written to its container.
Usage: lcl logs <project> [<service>]
  <project> (required) Project from which service logs are desired
  <service> (optional) Service for which to show logs; if omitted, shows logs from all services
Returns the content of the project's logs
```
##### Local Reload
```
Halts and restarts project containers
Usage: lcl reloadvm <project> [<service>]
  <project> (required) Project for which to reload service containers
  <service> (optional) Service for which to reload the container; if omitted, reloads all service containers
```
##### Local Status
```
Shows the status of the project's VM and its service containers.
Usage: lcl statusvm <project> [<service>]
  <project> (required) Project for which to show service container status
  <service> (optional) Service to show VM status; if omitted, shows status for all service containers
```
##### Local Start
```
Start all of a project's services
Usage: lcl startvm <projectId>
  <project> (required) Project for which to start the service VM
```
