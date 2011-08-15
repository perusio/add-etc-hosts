# Add/Remove hostnames from the /etc/hosts file

## Introduction

This script was created for simplifying the addition/removal of
hostnames to the `/etc/hosts` file. It's particularly useful if you're
developing a site locally and want that site to have a "handle" that
is related to the project name.

For example if I'm developing a site that is for a widget maker that
will use the domain mywidgetmaker.com I'll do:

    add-etc-hosts mywidgetmaker.com.local
   
Now I can enter `http://mywidgetmaker.com.local` on the address bar of the
browser and it will show me the site that I'm developing.

It's particularly useful for working with [Nginx](http://nginx.org), 
you just add the
[`server_name`](http://wiki.nginx.org/HttpCoreModule#server_name)
directive to your vhost configuration (server context), like this:

    server_name mywidgetmaker.local;  

## Installation

 1. Clone the repo from []() or [download]() it.
 
 2. Put the scripts in a directory included in your `PATH` or define
    aliases like this:
        
        alias add-etc-hosts='/path/to/add-etc-hosts'
        alias rm-etc-hosts='/path/to/rm-etc-hosts'
        
    Source the new aliases, if you have them in a `~/.bash_aliases` file:
    
        . ~/.bash_aliases
        
    or something similar, depending on the name and location of the
    files where the aliases are defined.    
        
 3. Done.
 
## Documentation
 
Full documentation is on the  manpage [`add-etc-hosts(8)`](http://github.perusio.org/add-etc-hosts).
