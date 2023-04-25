# port-to-process

Given a system port number, show what proccess is listening on the port.

Syntax:

    port-to-process <port number> ...

Example:

    port-to-process 80

Example to check ports for SSH, HTTP, IRC

    port-to-process 22 80 194


## Install

Option 1: download the file to wherever you want, then make it executable.

    cd /usr/local/bin/
    sudo curl -O https://raw.githubusercontent.com/SixArm/port-to-process/master/port-to-process
    sudo chmod +x port-to-process

Option 2: clone the repo to anywhere you want, then add it to your path.

    cd /anywhere/you/want
    git clone https://github.com/SixArm/port-to-process.git   
    export PATH="$PATH:/anywhere/you/want/port-to-process"

If you would like to help us by writing a package for any popular package manager, such as apt, yum, brew, etc., we wecome help.


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
  * Version: 4.1.1
  * Updated: 2023-04-25T11:13:34Z
  * License: GPL-2.0 or GPL-3.0 or contact us for custom
  * Contact: Joel Parker Henderson (http://joelparkerhenderson.com)
