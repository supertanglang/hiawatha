Hiawatha
========
Hiawatha is an open source webserver with security, easy to use and lightweight as the three key features. It supports among others (Fast)CGI, IPv6, URL rewriting and reverse proxy and has security features no other webserver has, like blocking SQL injections, XSS, CSRF and exploit attempts. Hiawatha runs perfectly on Linux, BSD and MacOS X.

The Hiawatha webserver has been written by Hugo Leisink <hugo@leisink.net>. More information about the Hiawatha webserver can be found at https://www.hiawatha-webserver.org/.

Installation
------------
If the CMake version installed on your system is lower than 2.8.4, remove it, download the latest version from http://www.cmake.org/cmake/resources/software.html and install it.

	tar -xzf cmake-<version>.tar.gz
	cd cmake-<version>
	./configure
	sudo make install

Use the following commands to compile and install Hiawatha. This will install Hiawatha in /usr/local.

	mkdir build
	cd build
	cmake .. [options]
	sudo make install/strip

The following options for cmake are available. Default value is in uppercase.

	-DENABLE_CACHE=ON|off              Enable internal cache support.
	-DENABLE_IPV6=ON|off               Enable IPv6 support.
	-DENABLE_MONITOR=on|OFF            Enable support for the Hiawatha Monitor.
	-DENABLE_RPROXY=ON|off             Enable reverse proxy support.
	-DENABLE_TLS=ON|off                Enable TLS (mbed TLS) support.
	-DENABLE_TOMAHAWK=on|OFF           Enable Tomahawk, the Hiawatha command shell.
	-DENABLE_TOOLKIT=ON|off            Enable the URL Toolkit.
	-DENABLE_XSLT=ON|off               Enable XSLT support.
	-DUSE_SYSTEM_MBEDTLS=on|OFF        Compile Hiawatha against the system's mbed TLS library (>=1.3.10).

The following path settings are available for cmake.

	-DCMAKE_INSTALL_PREFIX=<path>      The prefix for all other CMAKE_INSTALL directories.
	-DCMAKE_INSTALL_BINDIR=<path>      Location of the ssi-cgi binary.
	-DCMAKE_INSTALL_SBINDIR=<path>     Location of the other Hiawatha binaries.
	-DCMAKE_INSTALL_SYSCONFDIR=<path>  The configuration files will be installed in <path>/hiawatha.
	-DCMAKE_INSTALL_LIBDIR=<path>      The mbed TLS shared library will be installed in <path>/hiawatha.
	-DCMAKE_INSTALL_MANDIR=<path>      Manual pages will be installed in <path>/man1.
	-DCONFIG_DIR=<path>                Location of the Hiawatha configuration files.
	-DLOG_DIR=<path>                   Log directory used in the default hiawatha.conf.
	-DPID_DIR=<path>                   Location of the Hiawatha PID file.
	-DWEBROOT_DIR=<path>               Webroot directory used in the default hiawatha.conf.
	-DWORK_DIR=<path>                  Path of directory where Hiawatha can write temporary files.

Look inside the directory 'extra' for scripts to build packages for Debian, MacOS X and Windows (via Cygwin).

Related projects
----------------
The Hiawatha Monitor is a monitoring tool for Hiawatha. It helps you to keep track of all your Hiawatha installation. It's a PHP5 webapplication and requires a MySQL database and the cron daemon for periodic downloading of statistical information from the webservers it monitors. More information about the Hiawatha Monitor can be found at http://hiawatha-webserver.org/monitor.

The Banshee PHP framework has also been written with security in mind. It has a Model-View-Controller architecture (XSLT for the views) and requires a MySQL database. More information about Banshee can be found at http://www.banshee-php.org/.

Other interesting projects can be found at http://projects.leisink.net/.
