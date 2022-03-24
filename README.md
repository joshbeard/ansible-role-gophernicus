# Ansible Role for Gophernicus

This is an Ansible role for managing the deployment of the [Gopernicus](http://gophernicus.org/)
[Gopher](https://en.wikipedia.org/wiki/Gopher_(protocol)) server software.

This role was put together quickly for my particular deployment and has only been tested on Ubuntu 21.04.

Visit my Gopher hole at <gopher://jbeard.co>

## What This Role Does

* Installs the `gophernicus` package from OS repositories.
* Configures the Systemd service/socket
* Creates the content directories
* Manages the service/socket

## Variables

Refer to [defaults/main.yml](defaults/main.yml).

### gopher_hosts

Required list of hosts to serve.

This sets the `-h` argument and creates content directories.

Default: _none_

### gopher_data_dir

Path for hosting Gopher content.

Default: `/srv/gopher`

### gopher_start_args

Optional string of additional arguments to pass to the Gophernicus service.

Default: _none_
