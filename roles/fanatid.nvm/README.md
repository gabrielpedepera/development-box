# nvm

[![Build Status](https://img.shields.io/travis/fanatid/ansible-role-nvm.svg?branch=master&style=flat-square)](https://travis-ci.org/fanatid/ansible-role-nvm)

## Requirements

git, build-essential, libssl-dev

## Role Variables

  - `nvm.user` remote user
  - `nvm.version` nvm version tag, or HEAD
  - `nvm.node_version` node.js version

You can find default values in [defaults/main.yml](https://github.com/fanatid/ansible-role-nvm/blob/master/defaults/main.yml)

## Dependencies

No depedencies.

## Example Playbook

```
- hosts: servers
  roles:
    - role: fanatid.nvm
      nvm:
        user: deploy
        version: v0.33.0
        node_version: '7.0.0'
```

## LICENSE

This library is free and open-source software released under the MIT license.
