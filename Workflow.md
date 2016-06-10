
## Workflow
```
Workflow - Run an orchestrated and repeatable set of commands

Currently available workflow:

Name               Source  Description
----               ------  -----------
create-and-deploy  remote  Create, bootstrap, and deploy a Shipped project with one service
fast-deploy        remote  Fast bootstrap and deploy a Shipped project by name

Commands available for Workflow:
  List    List all workflow or the contents of a single workflow
  Help    Show help information for a workflow
  Resume  In console mode, resume execution of a workflow from the point of an error
  Run     Run a Shipped workflow

Use the run command to run a workflow, as follows:
shipped workflow run workflowName  [--var1 value1 [--var2 value2...]]
E.g.: shipped workflow run create-and-deploy --project xxx --service xxx --framework xxx [--env xxx] [fast=true]

To see help for an individual workflow, run command `shipped wf help workflowName`

```
##### Workflow List
```
List all workflow or the contents of a single workflow
Usage: wf get [<workflowName>]
  <workflowName> (optional) A regular expression to match against workflow names. If this argument is omitted or matches
                            more than one workflow, the command returns a list of workflows; if this argument matches a
                            single workflow, the command lists the entire workflow.
Returns either a list of workflows or the contents of a single workflow
```
##### Workflow Help
```
Show help information for a workflow
Usage: wf help workflowName
  
  workflowName (required) A regular expression matching the workflow for which help is desired.
Returns help for the requested workflow.
```
##### Workflow Resume
```
```
##### Workflow Run
```
```
