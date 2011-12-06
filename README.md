# node-profile

A script that makes profiling node.js apps a little easier.

## Installation

Via [npm](http://github.com/isaacs/npm):

    $ npm install profile

## Usage
### Output to stdout
`> nodeprofile yourapp.js`
### Output to file
`> nodeprofile yourapp.js -o=profile.txt`
### Lazy profiling (profiling disabled on startup)
This is useful if you want to profile certain areas of your code using [bnoordhuis/node-profiler](https://github.com/bnoordhuis/node-profiler):

`> nodeprofile yourapp.js --prof_lazy`

## "Dependencies"
* python
* [SCONS](http://www.scons.org/) (used to build the V8 debugger on first use) 
* That the `locate` command can find a copy of `linux-tick-processor` (or `mac-tick-processor` on OS X). This is bundled with node.js.

## Pre-configuration

    $ cd /usr/src/node
    $ cd deps/v8
    $ scons prof=on
    $ export PATH="${PATH}:/usr/src/node/deps/v8"

## Output

<img src="http://mape.me/nodeprofile.png" alt="">
