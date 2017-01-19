Introduction
============

[![Build Status][ciimg]][ci]
[![GoDoc][docimg]][doc]

The gousb package is an attempt at wrapping the libusb library into a Go-like binding.

Supported platforms include:

- linux
- darwin
- windows

[ciimg]:  https://travis-ci.org/kylelemons/gousb.svg?branch=master
[ci]:     https://travis-ci.org/kylelemons/gousb
[docimg]: https://godoc.org/github.com/karalabe/gousb?status.svg
[doc]:    https://godoc.org/github.com/karalabe/gousb

Contributing
============
Because I am a Google employee, contributing to this project will require signing the [Google CLA][cla].
This is the same agreement that is required for contributing to Go itself, so if you have
already filled it out for that, you needn't fill it out again.
You will need to send me the email address that you used to sign the agreement
so that I can verify that it is on file before I can accept pull requests.

[cla]: https://cla.developers.google.com/

Installation
============

Example: lsusb
--------------
The gousb project provides a simple but useful example: lsusb.  This binary will list the USB devices connected to your system and various interesting tidbits about them, their configurations, endpoints, etc.  To install it, run the following command:

    go get -v github.com/karalabe/gousb/lsusb

gousb
-----
If you installed the lsusb example, both libraries below are already installed.

Installing the primary gousb package is really easy:

    go get -v github.com/karalabe/gousb/usb

There is also a `usbid` package that will not be installed by default by this command, but which provides useful information including the human-readable vendor and product codes for detected hardware.  It's not installed by default and not linked into the `usb` package by default because it adds ~400kb to the resulting binary.  If you want both, they can be installed thus:

    go get -v github.com/karalabe/gousb/usb{,id}

Documentation
=============
The documentation can be viewed via local godoc or via the excellent [godoc.org](http://godoc.org/):

- [usb](http://godoc.org/github.com/karalabe/gousb/usb)
- [usbid](http://godoc.org/pkg/github.com/karalabe/gousb/usbid)
