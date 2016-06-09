Usage: shipped [options] [command [subcommand [args]]]

Options:
  -d  --debug        Provide TRACE logging
      --force        Do not prompt for confirmation when deleting a project or VM
  -f  --full         Show full model (all elements) in command responses
  -h  --help         Display help message for current command
  -i  --showids      Show UUIDs of objects in output
  -j  --json         Output command responses in JSON format
  -l  --latest       --latest option on build and release commands
      --log          Show logs after getting build (build get command)
      --logfile      Name of file to write log messages, including TRACE messages (also SHIPPED_CLI_LOGFILE) [default shipped-cli.log]
      --nohdr        Supress headers on command output
  -o  --output       Comma-separated list of output field names
  -p  --projectHome  Directory for Shipped projects (also SHIPPED_PROJECT_HOME)
  -x  --expanded     Include expanded descriptions in wizard workflow
  -s  --server       API server to access (also SHIPPED_API_SERVER) [default https://api.ciscoshipped.io]
  -t  --token        Shipped API authentication token (also SHIPPED_API_TOKEN)
  -v  --version      Show Shipped CLI version and exit
      --vm           Local VM manager (Vagrant or docker-compose) (also SHIPPED_VM) [default docker-compose]
  -w  --watch        Minutes to wait for build completion or release deployment (bld get or rlse get)

Commands [alias]:
  BuildPacks    [bp]    Language or framework base container for developing a service
  Builds        [bld]   Build status and logs for service
  Configs       [cfg]   Show and modify config for service
  Console       [con]   Shipped console (interactive command and response)
  Defaults      [dflt]  Show and set default IDs
  Environments  [env]   Deployment namespace management [e.g. dev, stage, prod]
  Local         [lcl]   Local [desktop] development environment management
  Projects      [pr]    Manage projects (collections of services and dependencies)
  Releases      [rlse]  Manage releases (service deployment snapshots)
  Run                   Run a Shipped workflow
  Services      [svc]   Manage services (independently deployable components of a project)
  Users         [usr]   Manage project users
  Wizards       [wz]    Interactive execution of a Shipped workflow
  Workflow      [wf]    Run an orchestrated and repeatable set of commands

Token is required the first time the shipped command is used.  It defaults to the previous value on subsequent
invocations.

Commands and arguments can be abbreviated by truncation to the minimum needed for unambiguous specification

To run the Shipped CLI console, type "shipped console"

To list subcommands for a command, type "shipped <command> --help".
For help on any subcommand, type "shipped <command> <subcommand> --help".
For information on Shipped orchestrated workflow, type "help workflow".
For information on default values and $ variables, type "help default".
For a guided tutorial introduction, type "wizard".
