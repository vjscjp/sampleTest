
## Run
```
Runs a Shipped CLI script
Usage: run scriptName [var1=value1 [var2=value2...]] [--help] [--verbose]
  scriptName (required) Name of the script to run.  Shipped looks for file scriptName.shipped first in
                        $HOME/.shipped/scripts and then on the Shipped API server
  var=value  (optional) Zero or more variable specifications.  Shipped replaces references of the form ${var[:default]}
                        with the value specified
  --help     (optional) Show help for the script. When this flag is used, Shipped shows help for the script instead of
                        running it.  Help is obtained directly from the script, and consists all lines whose first
                        non-blank character is "#".
  --verbose  (optional) list each script command before execution
Returns output from the commands in the script.  See help scripts for more on Shipped CLI scripts.

Currently available workflow:

Name               Source  Description
----               ------  -----------
create-and-deploy  remote  Create, bootstrap, and deploy a Shipped project with one service
fast-deploy        remote  Fast bootstrap and deploy a Shipped project by name
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
