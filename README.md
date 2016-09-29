# vpn-scripts
Scripts to use a Proxy with authentication through a Cisco Anyconnect VPN split tunnel

## Prerequisites

You need to have the following software installed on your machine:

- openconnect
- squid

On Mac OS you can install the components using [homebrew](http://brew.sh/) with the following commands:

    brew install openconnect
    brew install squid

## Configuration

Create a copy of `vpn.example.conf` and save it as `vpn.conf`.

Change the configuration in `vpn.conf` according to your needs.

## Start/Stop

To start the tunnel, proxy and change your system's configuration for the proxy type:

    ./vpn start

To stop the proxy, tunnel and clean your system's configuration from proxy settings type:

    ./vpn stop

If the tunnel collapses, because you've been idle, or whatever reason,
you can reestablish the tunnel connection with:

    ./vpn re

This command will not restart the proxy and will not reconfigure your system's proxy settings.

## Gimmicks

The npm script and configuration can help you configure npm for a corporate Nexus.
