# Debian package management

## List package

```bash
  ## list system package
  dpkg-query -l
  dpkg -l | less

  ## list python package
  dpkg -l 'python*'

  ## list installed package
  dpkg -l | grep '^.i'

  ## list installed package
  dpkg --get-selections | grep python

  ## list all installed packages with apt
  apt --installed list

  ## apt-show-versions tool (=>apt-get install apt-show-versions)
  apt-show-versions -r "python*"

```

## Packages in apt cache

```bash
  ## find packet containing token
  apt-cache search lxml

  ## show packet detail
  apt-cache show python-lxml

  ## show packet dependences
  apt-cache depends xen-tools

  ## show packet reverse dependences
  apt-cache rdepends build-essential

  ## show packet detail
  apt-cache show python-lxml

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
  dlocate /etc/nanorc
  apt-file search foo

```

