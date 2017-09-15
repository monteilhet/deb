# Debian package management

## List package

```bash
  ## list system packages
  dpkg-query -l
  dpkg -l | less

  ## list python packages
  dpkg -l 'python*'

  ## list installed packages
  dpkg -l | grep '^.i'

  ## list python packages
  dpkg --get-selections | grep python

  ## list all installed packages with apt
  apt --installed list

  ## list packages upgradable
  apt --upgradable list

  ## apt-show-versions tool (=>apt-get install apt-show-versions)
  apt-show-versions -r "python*"

```

## Packages in apt cache

```bash
  ## update cache
  apt-get update

  ## find packet containing token
  apt-cache search lxml
  
  ##  find packet containing token only in the package name
  apt-cache search lxml --names-only
  
  ## show packet detail
  apt-cache show python-lxml

  ## show packet dependences
  apt-cache depends xen-tools

  ## show packet reverse dependences
  apt-cache rdepends build-essential

  ## displays information about package (available versions and reverse dependencies)
  apt-cache showpkg python-lxml

  ## update cache for apt-file
  apt-file update

  ## package files list
  apt-file show xen-tools

  ## find the package that provides the specified file
  apt-file search /usr/bin/htpasswd

```

## Details on installed package

```bash
  ## package information
  dpkg --status xen-tools
  dpkg -s xen-tools
  ##  package status
  dpkg -s xen-tools | grep Status

  ## package files list
  dpkg --listfiles xen-tools
  dpkg -L xen-tools

  ## find the installed package that provides the specified file
  dpkg -S /etc/nanorc
  locate /etc/nanorc
  
```

## Policy

```bash

  ## show policy for the specified packet
  apt-cache policy mono-complete

```


## Download

```bash

  ## download .deb package without installing it
  aptitude download ripole

```
