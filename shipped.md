Usage: shipped [options] [command [subcommand [args]]]<br><br>Options:<br>  -d  --debug        Provide TRACE logging<br>      --force        Do not prompt for confirmation when deleting a project or VM<br>  -f  --full         Show full model (all elements) in command responses<br>  -h  --help         Display help message for current command<br>  -i  --showids      Show UUIDs of objects in output<br>  -j  --json         Output command responses in JSON format<br>  -l  --latest       --latest option on build and release commands<br>      --log          Show logs after getting build (build get command)<br>      --logfile      Name of file to write log messages, including TRACE messages (also SHIPPED_CLI_LOGFILE) [default shipped-cli.log]<br>      --nohdr        Supress headers on command output<br>  -o  --output       Comma-separated list of output field names<br>  -p  --projectHome  Directory for Shipped projects (also SHIPPED_PROJECT_HOME)<br>  -x  --expanded     Include expanded descriptions in wizard workflow<br>  -s  --server       API server to access (also SHIPPED_API_SERVER) [default https://api.ciscoshipped.io]<br>  -t  --token        Shipped API authentication token (also SHIPPED_API_TOKEN)<br>  -v  --version      Show Shipped CLI version and exit<br>      --vm           Local VM manager (Vagrant or docker-compose) (also SHIPPED_VM) [default docker-compose]<br>  -w  --watch        Minutes to wait for build completion or release deployment (bld get or rlse get)<br><br>Commands [alias]:<br>  BuildPacks    [bp]    Language or framework base container for developing a service<br>  Builds        [bld]   Build status and logs for service<br>  Configs       [cfg]   Show and modify config for service<br>  Console       [con]   Shipped console (interactive command and response)<br>  Defaults      [dflt]  Show and set default IDs<br>  Environments  [env]   Deployment namespace management [e.g. dev, stage, prod]<br>  Local         [lcl]   Local [desktop] development environment management<br>  Projects      [pr]    Manage projects (collections of services and dependencies)<br>  Releases      [rlse]  Manage releases (service deployment snapshots)<br>  Run                   Run a Shipped workflow<br>  Services      [svc]   Manage services (independently deployable components of a project)<br>  Users         [usr]   Manage project users<br>  Wizards       [wz]    Interactive execution of a Shipped workflow<br>  Workflow      [wf]    Run an orchestrated and repeatable set of commands<br><br>Token is required the first time the shipped command is used.  It defaults to the previous value on subsequent<br>invocations.<br><br>Commands and arguments can be abbreviated by truncation to the minimum needed for unambiguous specification<br><br>To run the Shipped CLI console, type "shipped console"<br><br>To list subcommands for a command, type "shipped <command> --help".<br>For help on any subcommand, type "shipped <command> <subcommand> --help".<br>For information on Shipped orchestrated workflow, type "help workflow".<br>For information on default values and $ variables, type "help default".<br>For a guided tutorial introduction, type "wizard".<br>