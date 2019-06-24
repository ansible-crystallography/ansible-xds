# crystal-multi-tool.xds

This role is in development.

A [Crystal-Multi-Tool](#) Ansible role to install the [XDS](http://xds.mpimf-heidelberg.mpg.de/) (**X**-ray **D**etector **S**oftware) suite and companion software.

## NOTE

XDS only allows non-commercial use of the software which this role installs. If you are a non-commerical user and agree to XDS's license, set the varaiable `xds_non_commerical` to yes.

## Tasks

### XDS

The task `xds.yml` installs the XDS core tools:
```
2cbf
cellparm
forkxds
mcolspot
mcolspot_par
merge2cbfi
mintegrate
mintegrate_par
pix2lab
xscale_par
xds
xds_par
xdsconv
xscale
```

### XDS Extras

The task `xds-extras.yml` installs XDS companion tools:
```
adxv
checkcentering
generate_XDS.INP
rlat4xds
spot2pdb
xds_nonisomorphism
XDS-viewer
xdscc12
xdsstat
xdsgui
xxdiff.centos7
xscale_isocluster
xscale_maxcc12
```

Additionally the follwing symlinks are created:
```
xxdiff -> /usr/bin/xxdiff.centos7
xscalecc12 -> /usr/bin/xdscc12
xds-viewer -> /usr/bin/XDS-viewer
xdsviewer -> /usr/bin/XDS-viewer
```

All of these files are hosted by the [Universität Konstanz](ftp://turn5.biologie.uni-konstanz.de/pub/linux_bin). Symlink conventions come from their installation suggestion.

### XDS Documentation

Installs documentation from XDS authors.

## TODO

- Add dependency software (XDSGUI?)
- Add xxdiff through yum and remove symlink
- Add env variables [see](http://xds.mpimf-heidelberg.mpg.de/html_doc/downloading.html)
