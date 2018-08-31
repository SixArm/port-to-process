# port-to-process

Given a system port number, show what proccess is running on the port.

Syntax:

    port-to-process <port number>

Example:

    port-to-process 80


## Install

Example 1: download the script to wherever you want, then make it executable.

    cd /usr/local/bin/
    sudo curl -O https://raw.githubusercontent.com/SixArm/port-to-process/master/port-to-process
    sudo chmod +x port-to-process

Example 2: clone the repo to wherever you want, then add it to your path.

    cd /foo/bar
    git clone https://github.com/SixArm/port-to-process.git   
    export PATH=$PATH:/wherever/port-to-process
    
    
## Implementation

This program aims to run on a wide variety of current Unix systems:

  * Debian, Ubuntu, Mint, etc.
  * RedHat, Fedora, CentOS, etc.
  * macOS

This program looks up the port information using a variety of commands such as:

  * `ss -lptn 'sport = :80'`

  * `lsof -n -i :80`

  * `netstat --numeric --listening --program | grep 80`

  * `fuser -v -n tcp 80`

  * `sockstat -4 -l | grep :80 | awk '{print $3}' | head -1`


## Tracking

  * Command: port-to-process
  * Version: 4.0.2
  * Updated: 2018-07-13
  * License: GPL
  * Contact: Joel Parker Henderson (http://joelparkerhenderson.com)
