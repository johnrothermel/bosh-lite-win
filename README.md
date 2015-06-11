# bosh-lite-win

A local environment to deploy Cloud Foundry with BOSH on Windows.

This readme documents the steps used to deply BOSH on Windows using Vagrant and Mobaxterm. The high level process is based off https://github.com/cloudfoundry/bosh-lite with some Windows specific deviations.


## Prereqs
* Must have processor that supports virtualization technologies like VTx and extended paging.

* Install [Mobaxterm](http://mobaxterm.mobatek.net/download-home-edition.html)

* Install [Mobaxterm Plugins](http://mobaxterm.mobatek.net/plugins.html)
 * Curl
 * DnsUtils
 * File
 * Git
 * Screen
 * Zip

  Place them in same directory as the Mobaxterm executable. 
   - Example: "C:\Program Files (x86)\Mobatek\MobaXterm Personal Edition"

* Install [Virtual Box for Windows](https://www.virtualbox.org/wiki/Downloads)
* Install [Vagrant](https://www.vagrantup.com/downloads.html)


  
  
