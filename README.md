# Icestudio

[![R&D](https://img.shields.io/badge/-R%26D-brightgreen.svg)](https://github.com/Jesus89/icestudio)
[![License](http://img.shields.io/:license-gpl-blue.svg)](http://opensource.org/licenses/GPL-2.0)

Experimental graphic editor for open FPGAs. Tested with Linux and [iCEstick board](http://www.pighixxx.com/test/portfolio-items/icestick/). Built on top of [icestorm project](http://www.clifford.at/icestorm/).

    GUI -> JSON -> Verilog, PCF

![][icestudio-demo]

## Installation

1. Install and configure the [drivers](https://github.com/FPGAwars/icestudio/wiki/Installing-the-drivers)

2. Download the [latest release](https://github.com/FPGAwars/icestudio/releases), unpack the zip and execute Icestudio

NOTE: this is an **early experimental version**. Initially supported on Linux (32, 64), Windows and Mac.

## Development

Install [nodejs](https://github.com/nodejs/node)
```bash
curl -sL https://deb.nodesource.com/setup_4.x | sudo -E bash -
sudo apt-get install -y nodejs
```

Install [nwjs](https://github.com/nwjs/nw.js)
```bash
sudo npm install -g nw@0.12.3
```

Install [nw-builder](https://github.com/nwjs/nw-builder)
```bash
sudo npm install -g nw-builder
```

Install [node-pre-gyp](https://github.com/mapbox/node-pre-gyp)
```bash
sudo npm install -g nw-gyp
sudo npm install -g node-pre-gyp
```

### Download

```bash
git clone https://github.com/FPGAwars/icestudio.git
cd icestudio
```

## Setup

```bash
npm install --prefix=icestudio

node-pre-gyp rebuild --directory=icestudio/node_modules/serialport --runtime=node-webkit --target=0.12.3
```

### Execute

```bash
nw icestudio
```

### Package

```bash
nwbuild -p linux64 icestudio -v v0.12.3
nwbuild -p osx64 icestudio -v v0.12.3
nwbuild -p win64 icestudio -v v0.12.3

cd build/Icestudio

zip -r icestudio-linux64 linux64
zip -r icestudio-osx64 osx64
zip -r icestudio-win64 win64
```

## Videos

[![Icestudio: GUI for open FPGAs](http://img.youtube.com/vi/Okl4Rr_i6Qk/0.jpg)](http://www.youtube.com/watch?v=Okl4Rr_i6Qk "Icestudio: GUI for open FPGAs")

[![Icestudio: code generation](http://img.youtube.com/vi/pG1DsF9MIj0/0.jpg)](http://www.youtube.com/watch?v=pG1DsF9MIj0 "Icestudio: code generation")

## Authors

* Jesús Arroyo

## Contributors

* Miguel Sánchez de León Peque

## Credits

* Using [AngularJS-Flowchart](https://github.com/codecapers/AngularJS-FlowChart)

## License

![][bq-logo-cc-sa]

Licensed under [GPLv2](http://opensource.org/licenses/GPL-2.0) and [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/)

[icestudio-demo]: doc/images/icestudio-demo.gif
[bq-logo-cc-sa]: doc/images/bq-logo-cc-sa-small-150px.png
