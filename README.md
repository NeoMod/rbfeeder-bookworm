# RBFeeder Debian/Raspbian packages

RBFeeder is a ADS-B client software used by [AirNav](https://www.radarbox.com/) 
to decode Mode S messages and send to our processing servers.

You can find more information about usage in [RadarBox](https://www.radarbox.com/) website.

This software is based on open-source softwares provided by 
Oliver Jowett (mutability) [dump1090-mutability](https://github.com/mutability/dump1090)
 and [FlightAware dump1090-fa](https://github.com/flightaware/dump1090)

It is designed to build as a Debian package, but should also be buildable on
many other Linux or Unix-like systems.

protobuf-c-compiler libncurses-dev libjansson-dev libglib2.0-dev libprotobuf-c-dev libcurl4-openssl-dev dh-sysuser devscripts librtlsdr-dev

## Building under bookworm

```bash
$ sudo apt-get install build-essential fakeroot debhelper librtlsdr-dev pkg-config libncurses5-dev protobuf-c-compiler libjansson-dev libglib2.0-dev libprotobuf-c-dev libcurl4-openssl-dev dh-sysuser devscripts librtlsdr-dev
$ git clone https://github.com/NeoMod/rbfeeder-bookworm.git
$ cd rbfeeder-bookworm/
$ dpkg-buildpackage -b
$ 
```
### dh-systemd is no longer needed since it has been merged into debhelper and the transitional package no longer exists.

### Actually building it

Nothing special, just build it (`dpkg-buildpackage -b`)

