---
layout: default
---

# Easy NodeJS version management

The easiest way to manage NodeJS versions on your PC is to use [nvm](https://github.com/creationix/nvm/blob/master/README.md).

The `nvm` command makes it easy for you to install a new version of NodeJS on your PC.
> Remember : after installing `nvm` you will need to restart your terminal window. To make sure the `nvm` command works from the terminal.

## Use it like this

To see which versions of NodeJS you have installed : `nvm ls`

To see which versions of NodeJS are available online : `nvm remote-ls`

To install a new version of NodeJS use : `nvm install <node_version>` to install NodeJS 8.3.0 use - `nvm install v8.3.0`

To set the default version of NodeJS - `nvm alias default v8.3.0`
