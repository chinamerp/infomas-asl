# README

This directory contains configuration files and information for setting up a
local development environment, compliant with the coding style and rules in use
at XIAM Solutions B.V.

## Recommended local development environment
This is the development software stack we are using ourselves. This stack is battle tested and
guaranteed to work.
+ Ubuntu Desktop 12.04.04 LTS (x64)
+ Oracle JDK, version 6u45 for building the open source artifacts
+ Oracle JDK, version 7u51 (for all other purposes)
+ Maven 3 (3.1.1) and Git 1.7 (1.7.9.5) available from shell
+ Netbeans IDE 8.0

## Target runtime environment (PRODUCTION)
Starting early 2010 all our server (production) environments are based on this stack. 
Currently (April 2014) this stack consists of:
+ Primary (and preferred) OS is Debian 7, also when using AWS EC2.
+ 64 bit
+ Oracle JDK, version 7
+ Tomcat 7

Both the local developments and the server environments are setup and managed by 
[ansible](http://ansible.cc). A highly recommended Software Configuration Management (SCM) 
tool.

## Checkstyle configuration
Checkstyle configuration files can be found in this directory and are referenced from the
parent Maven POM. If you are using Eclipse, you have to configure Eclipse using these files.
Note that Checkstyle warnings should be minimized. Checkstyle errors are always forbidden
and will make the build fail.

## Netbeans configuration
+ Both Oracle JDK version 6 and 7 should be installed
+ Install Netbeans (installation directory is references by $NETBEANS_HOME)
+ Run Netbeans using the Oracle JDK version 7. Add the following line in 
$NETBEANS_HOME/etc/netbeans.conf
```
netbeans_jdkhome="/usr/lib/jvm/java-7-oracle"
```
+ Import the standard configuration from this directory (netbeans-options.zip)
```
Tools > Options > Import > Select netbeans-options.zip > Select all options to import > OK
```
