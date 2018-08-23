[![Build Status](https://travis-ci.org/GeoffWilliams/puppet-realmd.svg?branch=master)](https://travis-ci.org/GeoffWilliams/puppet-realmd)
# realmd

#### Table of Contents

1. [Description](#description)
1. [Usage - Configuration options and additional functionality](#usage)
1. [Reference - An under-the-hood peek at what the module is doing and how](#reference)
1. [Limitations - OS compatibility, etc.](#limitations)
1. [Development - Guide for contributing to the module](#development)

## Description

Realmd support for RHEL

## Features

* Join a single domain
* Re-join to a different domain if `realm list --name-only` doesn't agree with the `domain` parameter
* `simple_allow_groups` used for access control

## Usage
See reference and examples

## Reference
[generated documentation](https://rawgit.com/GeoffWilliams/puppet-realmd/master/doc/index.html).

Reference documentation is generated directly from source code using [puppet-strings](https://github.com/puppetlabs/puppet-strings).  You may regenerate the documentation by running:

```shell
bundle exec puppet strings
```

## Limitations
* Not supported by Puppet, Inc.
* Supports joining a single realm only
* Rewrites `/etc/sssd/sssd.conf` (template)
* `simple_allow_groups` used for access control

## Development

PRs accepted :)

## Testing
This module supports testing using [PDQTest](https://github.com/declarativesystems/pdqtest).


Test can be executed with:

```
bundle install
make
```

See `.travis.yml` for a working CI example
