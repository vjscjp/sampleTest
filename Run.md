
## Run
```
```
##### Run create-and-deploy
```
Workflow create-and-deploy.shipped
  Create, bootstrap, and deploy a Shipped project with one service
  
  Usage:
  run create-and-deploy --project xxx --service xxx --framework xxx [--env xxx] [fast=true]
  
  Shipped prompts for any required variable not provided in the command line.
  
  Workflow arguments:
  project (prompted): the name of the project
  service (prompted): the name of the service
  framework (prompted): the name of the service framework
  env (optional, default "staging"): the name of the deployment environment
  fast (optional, default ""): specify fast=true for fast bootstrap
```
##### Run fast-deploy
```
Workflow fast-deploy.shipped
  Fast bootstrap and deploy a Shipped project by name
  
  Usage:
  run fast-deploy --project xxx --service xxx [--env xxx] [fast=false]
  
  Shipped prompts for project and service name if not provided.
  
  Workflow arguments:
  project (prompted): the name of the project
  env (optional, default "staging"): the name of the deployment environment
  fast (optional, default "true"): specify fast=false for full bootstrap (includes local vagrant VM)
  
```
