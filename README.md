# phpenv composer plugin

## What is this?
This plugin installs packages globally with `composer global require ...` and these separated by php versions in ~/.phpenv/versions/x.y.z/composer/ instead of ~/.composer/ by default.

## Requirements
This plugin is on the premise of installing https://github.com/phpenv/phpenv or its forks not https://github.com/CHH/phpenv.

## Install

```console
$ cd ~/.phpenv/plugins
$ git clone https://github.com/ngyuki/phpenv-composer.git
$ ln -fs ../plugins/phpenv-composer/libexec/composer ../bin
$ phpenv rehash
$ phpenv global 5.5.9
$ composer --version
Download composer.phar ...
#!/usr/bin/env php
All settings correct for using Composer
Downloading...

Composer successfully installed to: /tmp/composer.phar
Use it: php /tmp/composer.phar
Move composer.phar to /home/your/.phpenv/versions/5.5.9/composer
Composer version 714a47ef93d2387b66a6eff2cb9e2191c79b8d6d 2014-02-23 16:15:02
```

## Example

```console
$ composer global require phpunit/phpunit:\*
 :
$ phpenv rehash
$ phpenv which phpunit
/home/your/.phpenv/versions/5.5.9/composer/vendor/bin/phpunit

$ phpunit --version
PHPUnit 3.7.31 by Sebastian Bergmann.
```
