# Shell, init files, variables and expansions

## Init files
When invoked interactively with the --login option or when invoked as sh,
Bash reads the /etc/profile instructions. These usually set the shell variables
PATH, USER, MAIL, HOSTNAME and HISTSIZE.
On some systems, the umask value is configured in /etc/profile; on other systems 
this file holds pointers to other configuration files such as:

* /etc/inputrc, the system-wide Readline initialization file where you can configure the command line bell-style.
* the /etc/profile.d directory, which contains files configuring system-wide behavior of specific programs.

## Variables
Bash keeps a list of two types of variables:

### Global variables
Global variables or environment variables are available in all shells.
The env or printenv commands can be used to display environment variables. These programs come with the sh-utils package.

### Local Variables
Local variables are only available in the current shell. Using the set built-in command without any options will display a list of all variables (including environment variables) and functions. The output will be sorted according to the current locale and displayed in a reusable format.


## Expansions
Each time we type a command line and press the enter key, bash performs several processes upon the text before it carries out our command. We have seen a couple of cases of how a simple character sequence, for example “*”, can have a lot of meaning to the shell. The process that makes this happen is called expansion. With expansion, we type something and it is expanded into something else before the shell acts upon it.
