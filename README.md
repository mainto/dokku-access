# dokku-userAccess [![Build Status](https://img.shields.io/travis/mainto/dokku-access.svg?branch=master "Build Status")](https://travis-ci.org/mainto/dokku-access)

*User Access Control for Dokku.* 

This plugin adds user access control (Command permission, Git - push/pull for each App)

## requirements

- dokku 0.4.0+
- docker 1.8.x

## installation

```shell

# on 0.4.x
dokku plugin:install https://github.com/mainto/dokku-access.git access
```

## commands

```shell
access:admin                     Show list of admins with access to run all command
access:admin-add <user>          Allow users access to run all command
access:admin-remove <user>       Revoke users access to run all command
access:admin-removeAll           Revoke all users access to run all command
access:git <app>                 Show list of users with access to app repository
access:git-add <app> <user>      Allow user access to the app repository
access:git-remove <app> <user>   Revoke users access to the app repository
access:git-removeAll <app>       Revoke all users access to the app repository
```

### defining users

using dokku ssh-keys command, you can add or remove users to dokku.

### default behavior

By default root or admin can run command and access to repositories.
Using dokku access command, you can give access to users.
