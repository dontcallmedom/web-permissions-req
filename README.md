#Permissions for Web APIs

Web APIs that expose sensitive data or hardware features are usually gated by user consent in browsers.

That user consent can take several forms, and be exposed to developers through various mechanisms.

This repository collects [examples of these various user consent approaches](tests/) and documents how they are handled by existing browsers via [screenshots](screenshots/).

The variety of approaches is [documented in a matrix]http://dontcallmedom.github.io/web-permissions-req/matrix.html) relating APIs with their permission mechanisms analysed through various parameters:
* type of the consent mechanism (e.g. prompt vs implict user interaction)
* timing of the consent (upfront vs at usage time)
* persistence of the permission
* visual feedback on which permissions are currently granted (e.g. via persistent or transient state indicators)
* whether any UI exposes ways for users to control (e.g. revoke or restrict) the permissions
* how embedding (via an iframe) affects the availability of the permission request
* how developers can determine they've been denied access to the feature
