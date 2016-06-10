
```
## Environments
```
Environments - Deployment namespace management [e.g. dev, stage, prod]

Commands available for Environments:
  Create  Create a project environment
  Delete  Delete a project environment
  Get     Get a project environment or all of a project's environments
  GetAll  Get all environments
  Set     Set the default environment ID
```
##### Environments Create
```
Create a project environment
Usage: environment create <project> name=xxx [description=xxx]
  <project>       (required) The project for which to create the environment
  Name=xxx        (required) The name of the environment
  Description=xxx (optional) A description of the environment
Returns an Environment struct
```
##### Environments Delete
```
Delete a project environment
Usage: environment delete <project> <environment>
  <project>     (required) The project for which to delete an environment
  <environment> (required) The environment to delete
Returns "OK" if successful
```
##### Environments Get
```
Get a project environment or all of a project's environments
Usage: environment get <project> [<environment>]
  <project>     (required) The project for which to list environment(s)
  <environment> (optional) The environment to list; if omitted, lists all environments
Returns either an Environment struct or an array of Environment structs
```
##### Environments GetAll
```
Get all environments
Usage: environment getall <project>
  <project> (required) The project for which to list environment(s)
Returns an array of Environment structs
```
##### Environments Set
```
Set the default environment ID
Usage: buildpack set <environment>
  <environment> (required) The environment to set as the default
Returns "OK" if successful
```
