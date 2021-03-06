# Mockingj

A fork on [Laravel/Homestead](https://github.com/laravel/homestead) in [CentOS 7](https://www.centos.org) in VirtualBox VM Environment.

Mockingj is a wrapper of `vagrant` command, developed to be used together with [Mockingj Vagrant Box](https://atlas.hashicorp.com/justinmoh/mockingj).

## Includes

* CentOS 7.2
* VirtualBox Guest Additions (v5.0.12)
* Nginx (Mainline 1.9.x)
* MariaDB 10.1
  * Username: mockingj
  * Password: secret
* Postgresql 9.4
* Sqlite 3.9
* PHP 7.0.1
* Xdebug
* Composer
* Git 2.6.4
* NodeJS v5


## Installation

1) Add vagrant box

```bash
vagrant box add --box-version 0.4.7 justinmoh/mockingj
```

2) Get `mockingj` with composer

```bash
composer global require justinmoh/mockingj=^1.0.11
```

3) Init the application

```bash
cd ~/.composer/vendor/justinmoh/mockingj/ && sh init.sh
```

4) Configure

```bash
open ~/.mockingj/mockingj.yaml
```

5) Edit `/etc/hosts` in host (local) machine and add the following:

> 192.168.20.20     mockingj.dev

6) UP!

```bash
mockingj up
```



## Default Forwarded IP and Ports

```
ip: "192.168.20.20"
```

```
default_ports = {
  80   => 8001,
  443  => 44301,
  3306 => 33061,
  5432 => 54321
}
```

## Vagrant Boxes

### Based On
* [CentOS/7 (v1509.1)](https://atlas.hashicorp.com/centos/boxes/7/versions/1509.01)

### Extended VM required
* [justinmoh/mockingj](https://atlas.hashicorp.com/justinmoh/mockingj)

