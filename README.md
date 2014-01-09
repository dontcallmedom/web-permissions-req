#Permissions for Web APIs

Web APIs that expose sensitive data or hardware features are usually gated by user consent in browsers.

That user consent can take several forms, and be exposed to developers through various mechanisms.

This repository collects [examples of these various user consent approaches](tests/) and documents how they are handled by existing browsers via [screenshots](screenshots/).

The variety of approaches is [documented in a matrix](http://dontcallmedom.github.io/web-permissions-req/matrix.html) relating APIs with their permission mechanisms analysed through various parameters:
* type of the consent mechanism (e.g. prompt vs implict user interaction)
* timing of the consent (upfront vs at usage time)
* persistence of the permission
* visual feedback on which permissions are currently granted (e.g. via persistent or transient state indicators)
* whether any UI exposes ways for users to control (e.g. revoke or restrict) the permissions
* how embedding (via an iframe) affects the availability of the permission request
* how developers can determine they've been denied access to the feature

## Features
The features in the matrix are the ones that matched the following criteria:
* they are currently implemented in a deployed browser
* I could run them in my own set up
* I knew they were gated by user consent

The following features are designed to require user consent but have not been included in the matrix (yet):
* push API
* network service discovery
* Web MIDI
* Web Crypto for key reuse
* application cache (only Firefox prompt on this currently)

Also, some APIs have been deemed as safe enough to be usable without user consent, but recent research could push toward revisiting them. For instance, access to the accelerometer has been proved to leak information on e.g. what a user would type on a separate keyboard, or on the device itself, and might need mitigation (e.g. only run when tab is being displayed by default).

## Parameters of the analysis
Beyond the current parameters in the matrix, it would be interesting to also look at:
* whether page visibility affects the permission model (it does e.g. for fullscreen)

## TODO
* gather screenshots on more browsers, on more devices
* increase the number of tested features
* make tested features work on more browsers where possible (i.e. look at more vendor-prefixes)
