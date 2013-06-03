# puppet-boilerplate

A puppet module for managing and configuring boilerplate

## Testing

[![Build Status](https://travis-ci.org/electrical/puppet-boilerplate.png?branch=master)](https://travis-ci.org/electrical/puppet-boilerplate)

## Usage

Installation, make sure service is running and will be started at boot time:

     class { 'boilerplate': }

Removal/decommissioning:

     class { 'boilerplate':
       ensure => 'absent',
     }

Install everything but disable service(s) afterwards:

     class { 'boilerplate':
       status => 'disabled',
     }

Disable automated restart of boilerplate on config file change:

     class { 'boilerplate':
       restart_on_change => false
     }
