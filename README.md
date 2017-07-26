# Puppet Windows MUS custom provider

## Introduction

This module has been cloned from the https://github.com/mansong1/puppet-msu.git.
Provides the ability to install MSU packages in Windows only, using the WSUA.exe
program via Puppet.

## How to Use

In order to use this module:

In the Puppetfile (r10k):

```
mod 'tsw_windows-msu',
  :git    => 'https://github.com/rentsmartUK/puppet-tsw_windows-msu.git',
  :tag    => 'v0.1'
```

Specify the provider for the package resource:

```ruby
package { 'MyMSUpackage.msu':
  ensure    => present,
  source    => 'c:/MyMSUpackage.msu',
  provider  => msu,
}
```
