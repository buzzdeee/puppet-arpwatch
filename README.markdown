#arpwatch

##Overview

This Puppet module installs, configures and manages the Arpwatch daemon.

##Setup

###What arpwatch affects

* arpwatch package.
* arpwatch service configuration file.
* arpwatch service.

##Usage

```puppet
include '::arpwatch'
```
##Reference

###Public Classes

* arpwatch: main class.

###Public Parameters

####`package_ensure`

Sets the arpwatch package to be installed. Can be set to 'present', 'latest', or a specific version.

####`package_name`

Determines the name of the package to install. *Defaults to 'arpwatch'*.

####`service_enable`

Determines if the service should be enabled at boot.

####`service_ensure`

Determines if the service should be running or not.

####`service_name`

Selects the name of the arpwatch service for Puppet to manage. *Defaults to 'arpwatch'*.

####`ethercodes_file`

Provide an updated ``ethercodes.dat`` file.  This should be in the Puppet
URI scheme.

##Limitations

This module has been tested on Puppet 3.5.0 but should work on:

* Puppet 3.x and higher.

The module has been tested on Ubuntu 13.10 but should work on the
latest stable releases of:

* Ubuntu
* Debian
* Fedora
* RedHat

Though, given the lack of frequent updates to arpwatch and its
packaging in most distributions, the module should work on all RedHat
and Debian distrbution variants.

There is currently no support for the Debian-specific
/etc/arpwatch.conf file for configuring individual options (though the
intention to support it eventually is there).
