Bitmessage PHP Class
====================

[![tip for next commit](http://prime4commit.com/projects/112.svg)](http://prime4commit.com/projects/112)

[Bitmessage](https://bitmessage.org/) PHP Class to control PyBitmessage daemon using xmlrpc


Release Information
---------------
This repo contains in-development code for future releases. To download the
latest stable release please visit the [release](https://github.com/Conver/class.bitmessage.php/releases) page.


Requirements
---------------
php5-xmlrpc

php5-curl

Getting Started
---------------
1. Make sure php5-xmlrpc & php5-curl is installed and loaded
    
  `apt-get install php5-xmlrpc php5-curl`

  `service apache2 restart`

2. Include class.bitmessage.php into your PHP script:

	`require_once('curl.php');`
	
	`require_once('class.bitmessage.php');`
    
3. Initialize Bitmessage connection/object:

	`$bitmessageObj = new bitmessage("<RPCusername>:<RPCpassword>@<RPChost>:<RPCport>/");`

	Optionally, you can turn off the class stt protocol (HTTP and HTTPS). Default  protocol is http.

	`$bitmessageObj = new bitmessage("<RPCusername>:<RPCpassword>@<RPChost>:<RPCport>/", "http");`
    
4. Make calls to Bitmessage daemon as methods for your object. Examples:

    `$bitmessageObj->newAddress($label, $eighteenByteRipe = false, $totalDifficulty = 1, $smallMessageDifficulty = 1);`
    
    `$bitmessageObj->setStrip(true);`
    
    `$bitmessageObj->broadcast($address, $title, $message);`
    
Features
========

* Automatic Decoding
* Automatic HTML strip
* Support SSL over HTTPS
* Clean arrays (JSON decoded)

    
Contributing
============

You can contribute to this project in different ways:

* Report outstanding issues and bugs by creating an [Issue](https://github.com/Conver/class.bitmessage.php/issues/new)
* Suggest feature enhancements via our [Forum Thread](https://bitmessage.org/forum) on bitmessage forum
* Fork the project, create a branch and file a pull request to improve the code itself

Contact
=======

Bitmessage: BM-NBH4Q94X9E6mNmdKqeF68zWC4uzz7uCB

Donations
=========

Donations to this project are going directly to [Conver](https://github.com/Conver), the original author of this project:

* BTC address: `1Ac9HwAg352hWepY51jhPncGDwrrQWftT7`


LICENSE
---------------
Copyright (C) 2014 - 2014  Convertor

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>
