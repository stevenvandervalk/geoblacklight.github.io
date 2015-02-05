---
layout: tutorial-c4l
title:  Setting up your environment - Part 2 - Code4Lib 2015 Workshop"
date:   2015-02-09 14:58:00
categories: tutorial
author: 'Jack Reed'
author_link: 'https://twitter.com/mejackreed'
snippet: 'Setting up your development environment for GeoBlacklight. Created as part of a tutorial series for a 2015 Code4Lib Preconference Workshop'
---

## Setting up your environment
  - Development requirements
  - Local attendees setup VirtualBox/Vagrant

### Development requirements

GeoBlacklight has similar prerequisites to [Blacklight][blacklight]. It diverges from Blacklight requirements by using a customized Solr schema and configuration, [Geoblacklight-Schema][geoblacklightschema].

#### Software you should have installed on your development computer

  - [Ruby > 1.9.3][installruby]
  - [Rails > 4][installrails]
  - [Git][installgit]
  - Java (for local Solr server)

Local attendees of the workshop have the option of just using the pre-created environment on the provided thumb-drive.

### Local attendees setup VirtualBox/Vagrant
  
Good news for local workshop participants, this is already done for you using VirtualBox and Vagrant. On the thumb-drive underneath a directory titled 'geoblacklight_workshop'. Thanks to Justin Coyne and [Data Curation Experts](http://curationexperts.com/) for this approach that is used at HydraCamps.

For those interested in what was installed on this machine and how it was created checkout [this gist](https://gist.github.com/mejackreed/727e9cd2e971ca3949a2).


#### Vagrant
  1. Install either the Windows (.exe) or Mac (.dmg) version of VirtualBox on your machine along with Vagrant.
  1. Make a new directory for your work

    ```sh
    $ mkdir ~/scratch
    ```

  1. Copy the `geoblacklight_workshop` directory to your `~/scratch` directory

  1. Move to your `~/scratch` directory

    ```sh
    $ cd ~/scratch
    ```

  1. Start vagrant

    ```sh
    $ vagrant up # This command creates and configures guest machines according to your Vagrantfile.
    ```

  1. SSH to the VM

    ```sh
    $ vagrant ssh # This will SSH into a running Vagrant machine and give you access to a shell.
    ```

<div class='flash-notice'>
  <a href="{% post_url 2015-02-09-create-your-application %}">Next → Part 3 - Create your application</a>
</div>

[geoblacklight]:        http://geoblacklight.org
[geoblacklightproject]: /projects/geoblacklight
[geoblacklightschema]:  https://github.com/geoblacklight/geoblacklight-schema
[installruby]:          https://gorails.com/setup#ruby
[installrails]:         https://gorails.com/setup#rails
[installgit]:           https://gorails.com/setup#git
[rubyonrails]:          http://rubyonrails.org/
[blacklight]:           http://projectblacklight.org/