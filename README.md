[![Snap Status](https://build.snapcraft.io/badge/ogra1/xdmcp-client.svg)](https://build.snapcraft.io/user/ogra1/xdmcp-client)

# xdmcp-client snap
Minimal XDMCP thin-client snap to use with mir-kiosk

## Install/Setup (on Ubuntu Core)

#### Make sure to run the latest core snap from edge (only there you will find the required features)

snap refresh --edge core

#### Enable the layouts feature

snap set core experimental.layouts=true

#### Install mir-kiosk

snap install --edge mir-kiosk

#### Connect the required interfaces

snap connect xdmcp-client:wayland-socket-dir mir-kiosk:wayland-socket-dir

snap connect xdmcp-client:x11-plug xdmcp-client:x11

#### Restart the xdmcp-client snap

snap stop xdmcp-client

snap start xdmcp-client

## Running

After restarting the xdmcp-client an input field should show up on your screen, put in the IP (or the name if your server is known via DNS by the client) and an XDMCP session should start allowing you to remotely log in to the server desktop.
