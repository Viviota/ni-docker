# Quick Reference
- **Maintained by** Viviota, Inc.

# About this Repository
This repository contains docker build files related to NI software.
The built containers can be downloaded from [docker hub](https://hub.docker.com/u/viviota)
Containers are built on the server/servercore images by Microsoft.

Currently this repo supports ONLY LabVIEW Runtime 64-bit and NI Package Manager images.
Extension to 32-bit images would be possible, but is not done at this time.

Additional container options are under consideration as well.

We keep the docker containers very simple, and will update docker hub tags as new verisons of NIPM and LabVIEW are released.

# Using the LabVIEW Runtime Image
This image includes only the LabVIEW Runtime Engine, and is intended as a base image for deployment / execution of LabVIEW applications.

It ***does not*** include the LabVIEW Development Environment, and cannot be used for build, compile, or CI/CD purposes.  Though some such repositories are created/maintained [elsewhere](https://hub.docker.com/r/felipefoz/labview).

# Extending this Image
NI Package Manager is installed on this image, and the working directory is set to that install location.  the [**NIPM Command Line Interface**](https://www.ni.com/docs/en-US/bundle/package-manager/page/cli-package-manager.html) can be invoked to register new (public or private) feeds.

# Licenses
### NI LabVIEW
The usage of LabVIEW is governed by the [**NI Software License Agreement**](https://www.ni.com/content/dam/web/pdfs/legal/software_license_agreement_en.pdf) and the LabVIEW Runtime Engine is free to use & distribute.

LabVIEW is Copyright 2023 National Instruments Corporation.  All Rights Reserved.

### This Image
This image is maintained and distributed by [**Viviota, Inc**](https://www.viviota.com) and is governed by the [**MIT license**](https://opensource.org/license/mit/), as follows

Copyright 2023 Viviota, Inc.
Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
