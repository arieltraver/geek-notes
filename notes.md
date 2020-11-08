# Welcome to Ari's Shell notes!

## _Becoming a Super User one trick at a time._

## The basics

### _Let's hope I never forget..._
* cd: change directory
	* "cd .." = go to the parent director
	* "cd - " = go to the last directory you were in
* cp: copy
* mkdir: make a directory
* exit: quit the shell
* rm: remove
* mv: move
* pbcopy: paste to clipboard
* recursively remove everything in a directory

	```sh
	rm -r ./path/to/dir
	```

* ls: list the contents of the current directory
	*"ls -v" = list even files the computer doesn't feel like showing you
	*"ls -A" = list ALL files no matter what, including .git!
* vi: open a document with mac builtin vim
	* downloa neovim for a better terminal editor
* homebrew: a useful package manager
	* install online, then use "brew install" or "brew cask install" to get whatever you want! see brew's man page for more details.
* coreutils: the stuff from GNU that we wish we had, if apple would stop being apple
	* commands start with g (for example, gsleep) but this can be changed
* echo: print exactly what you typed

## Lesser Known Tools
* sips: image processing, converts to different filetypes
	* To heck with those pesky HEICS!
	* example: sips -s format jpeg filename.gif --out newfilename.jpg
* tcpdump: get network connections
	* example: 
	```sh
	tcpdump -i en0 -v -f "output.pcap"
	```
	* must be run with sudo
* launchctl: manage daemons
	* must be run with sudo
* curl: a lovely tool which fetches data from a website using HTTPS
	* returns either the raw html OR nicely formatted info if the website authors made one for use with curl
	* run with -q to block statistics
* ping: send an ICMP ping to a remote device
	* specify either IP address or domain name
* traceroute: send a series of packets to a remote device that expire early, revealing the route
	* I think the default is UDP
	* Not 100% reliable; depends on network routing protocols
	* The packets expire and a "ttl expired" message is sent back from each hop along the way
* ssh: Log into a remote machine or server using an SSH connection
	* Public keys can be configured in the ~/.ssh directory to avoid having to log in every time
* find: helps locate files which may be any which where on your computer
	* example:
	```sh
	find /Users -name "example.txt"
	```
* gcc: compile a c file into an executable
	* example:
	```sh
	gcc -o "test.c" -Wall -Werror
	```
tee: copies output to files 
    options: -a = append
