Cobweb Plot 2008
================
This application can be used to visualize a cobweb plot of a function.

It was developed at [Ball State University](http://www.bsu.edu) and [Emporia State University](http://www.emporia.edu/) 
by [Richard Stankewitz](http://www.bsu.edu/web/rstankewitz/), [Joe Yanik](http://www.emporia.edu/math-cs/yanikjoe/),  and Ben Dean.


Requirements
------------
Cobweb Plot 2008 will run on systems with the following:

* Java Runtime Environment version 6 or greater (JRE 8 recommended)
* An OpenGL graphics card.
* Windows, Mac OS X, Linux, or Solaris operating systems


Installation and Use
--------------------
Cobweb Plot 2008 can be launched as a Java Web Start Application:

* [Cobweb Plot 2008 - v1.1.0 (stable)](https://bsumath.github.io/cobweb2008/jnlp/cobweb2008.jnlp)

For information about using Cobweb Plot 2008 offline, please refer to the
[Installation instructions](https://github.com/bsumath/cobweb2008/wiki/Installation) on the wiki.

Development
-----------
Development requirements:

* Java SE Development Kit 8 or higher
* Groovy 2.4.4 or higher
* Gradle 2.6 or higher
* IntelliJ IDEA (recommended IDE)

### Build
To build Cobweb Plot 2008 run:

    gradle build

### Release
To release a new version of Cobweb Plot 2008, in addition to building the project you need to sign the jar files with a certificate. Rich Stankewitz keeps the BSU Math department's signing key.

Create a file in this repo named `keystore.properties` with the following:

    storepass=the key store password goes here
    storetype=pkcs12
    keystore=D:\\path\\to\\the\\cert.p12
    alias=the correct certificate alias
    tsaurl=http://the.real.timestamp.authority.example.com

Rich Stankewitz has the correct values for the `keystore.properties` file. Once that file is created you can sign the jars and generate the jnlp content with:

    gradle createWebstart

Then the `build/jnlp` directory will contain

* `cobweb2008.jnlp` - the file to launch Cobweb Plot 2008 via Java Web Start
* `lib/*.jar` -  the signed jar files for Cobweb Plot 2008 and its dependencies

These files should then be committed on the [bsumath/cobweb2008@gh-pages](https://github.com/bsumath/cobweb2008/tree/gh-pages) branch.

Contributors
------------
* [Richard Stankewitz](http://www.bsu.edu/web/rstankewitz/)
* [Joe Yanik](http://www.emporia.edu/math-cs/yanikjoe/)
* Ben Dean

License
-------
Copyright © 2008-2016 Ball State University

Copyright © Emporia State University

Cobweb Plot 2008 is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

Cobweb Plot 2008 is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with Cobweb Plot 2008.  If not, see <http://www.gnu.org/licenses/>.