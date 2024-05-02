[![Snap Status](https://build.snapcraft.io/badge/ogra1/xdmcp-client.svg)](https://build.snapcraft.io/user/ogra1/xdmcp-client)

# xdmcp-client snap
Minimal XDMCP thin-client snap to use with ubuntu-frame

## Install/Setup (on Ubuntu Core)

#### Install ubuntu-frame

    snap install ubuntu-frame

#### Install the client and then point it to an XDMCP server

    snap install xdmcp-client

(The client will not start before you have pointed it to
an XDMCP server)

    snap set xdmcp-client xdmcp-server="<IP of your XDMCP server>"
