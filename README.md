# COMMAND LINE INTERFACE (CLI) INTRODUCTION
## 1. Terminology
Node: A VM in the cluster
NodeGroup: A group of VMs with same functionality and spec
Cluster: A group of NodeGroups working together
Distro: A Hadoop distribution version

## 2. Usage
CLI supports shell mode, command line mode, and execution of script file. After compile, you can find the jar file under cli/target directory.
- Shell mode: java -jar serengeti-cli-0.1.jar. It supports tab key based command hint and completion. It supports history by up/down arrows.
- Command line mode: java -jar serengeti-cli-0.1.jar "command1;command2..."
- Execution of script file: in shell mode or command line mode, execute "script --file scriptFileName". The shell history file named cli.log will help to generate the script file. 

## 3. Command Syntax
CLI commands are built on spring shell(https://github.com/SpringSource/spring-shell), so its syntax follows spring shell command syntax below:
Command ::= serengeti <command-category> <command-name> <required-command-key-values>* [<optional-command-key-values>]*
required-command-key-values ::= <command-key-value-fullsize>
optional-command-key-values ::= <command-key-value-fullsize>
required-command-key-values-fullsize ::= <command-key-value-fullsize>
optional-command-key-value-fullsize ::= <command-key-value-fullsize>
command-key-value-fullsize ::= '--'<command-key-full> [<value>]
- Command-category is the type of object that the command will operate on.
- Command-name is the operation to do.
- Required-command-key-values are parameters that required for the operation.
- Optional-command-key-values are parameters that are optional for the operation.

## 4. Command Help
- Shell level Help: user can get shell level help by using "help" in command line mode or help command in shell mode. A list of objects will be displayed with operations and short descriptions.
- Command category level help: to get help for a particular class of object, user can enter help followed by an object. CLI will display all operations defined for the object.
- Command level help: to get help for a particular operation, user can enter help followed by an object and an operation. This will display all parameters.

## 5. Command List