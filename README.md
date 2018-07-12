# port-to-process

Given a system port number, show what proccess is running on the port.

Syntax:

    port-to-process <port number>

Example:

    port-to-process 80


## Implementation

This program aims to run on a wide variety of current Unix systems:

  * Debian, Ubuntu, Mint, etc.
  * RedHat, Fedora, CentOS, etc.
  * macOS

This program looks up the port information using a variety of commands:

  * ss
  * lsof
  * netstat
  * sockstat
  * fuser


## Tracking

  * Command: port-to-process
  * Version: 4.0.0
  * Updated: 2018-07-12
  * License: GPL
  * Contact: Joel Parker Henderson (http://joelparkerhenderson.com)
