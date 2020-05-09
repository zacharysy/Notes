# Useful Bash Commands
## `env`
* See all variables

## `$<var>`
* Access variable
* Assignment: `$<var>=<val>`

## `man <command>`
* Search with `/word`

## `source <file>`
* executes a file

## `cd -`
* return to previous directory

## `su <user>`
* Change user

## `stat <file>`
* Gives information about a file

## `<commnad>&`
* Run process in background

## `jobs`
* See jobs
* if process is a job can kill with `kill %n`
	* where `n` is the nth job

## `ip addr`
* Get ip addresses

## `host`
* hostname info

## `dig` 
* dns lookup utility

## `ss -tlp`
* scan ports on local machine

## `nmap -v -Pn <hostname>`
* Scan ports on hostname


## `nc`
* Bunch of networking stuff

## `traceroute <hostname>`
* See how many hops it takes to reach server

## `${<variable>:-<value>}`
* Set default values

## `export <thing>`
* Get variables from environment

## `source <file>`
* Get variables from child

## `#?`
* Exit status of last command

## `[ -e ]`

## `ps aux`
* See all the proceses

## `wc -l`
* Count lines

## `sort | uniq -c`
* Shows unique lines and count
* `uniq` assumes ordered list, so have to sort

## `tee`
* Copy stdin to stdout

## `sed`
* `-e <pattern> -e <pattern> ...` do multiple expressions
* `-n` print only lines matches