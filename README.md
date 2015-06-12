# bosh-lite-win

A local environment to deploy Cloud Foundry with BOSH on Windows.

This readme documents the steps used to deply BOSH on Windows using Vagrant and Mobaxterm. The high level process is based off https://github.com/cloudfoundry/bosh-lite with some Windows specific deviations.

Mobaxterm is currently my favorite terminal emulator for Windows and there are specific steps to make it work with vagrant and git.

## Prereqs
* Processor that supports virtualization technologies like VTx and extended paging.
* 8GB RAM 
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

## Configure Vagrant and Mobaxterm
1. Change ```#!/usr/bin/env bash``` to ```#!/usr/bin/env.exe bash``` in ```/drives/c/HashiCorp/Vagrant/bin/vagrant```
 * Without the exe extension Mobaxterm gets confused.

2. Append Windows PATH environment
 * Start Mobaxterm and navigate to Settings -> Configuration -> Terminal
 * Check "Use Windows PATH environment" if not already done
 * Restart Mobaxterm and run vagrant or git to verify they are found.

## Setup curl certs for git
1. Save [curl-ca-bundle.crt](https://github.com/johnrothermel/bosh-lite-win/blob/master/curl-ca-bundle.crt) in your Mobaxterm home directory or some other safe place like ~/certs.
2. Configure git to use the curl cert and clone this repository. Must specify ```/home/mobaxterm``` and not ```~``` for git config.
```
$ git config --global http.sslcainfo /home/mobaxterm/PATH-TO/curl-ca-bundle.crt
$ git clone https://github.com/johnrothermel/bosh-lite-win.git
```

## 
 

 
  
  
