class.bitmessage.php
====================

Bitmessage PHP Class to control PyBitmessage daemon

Requirements
---------------
php5-xmlrpc

apt-get install php5-xmlrpc

Getting Started
---------------
1. Make sure php5-xmlrpc is installed and loaded
    
  `apt-get install php5-xmlrpc`
  `service apache2 restart`

2. Include class.bitmessage.php into your PHP script:

	`require_once('class.bitmessage.php');`
    
3. Initialize Bitcoin connection/object:

	`$bitmessageObj = new bitmessage("<RPCusername>:<RPCpassword>@<RPChost>:<RPCport>/");`

	Optionally, you can turn off the class autoload & stt protocol (HTTP and HTTPS). Default autoload is true, protocol is http.

	`$bitmessageObj = new bitmessage("<RPCusername>:<RPCpassword>@<RPChost>:<RPCport>/", "http", false);`
    
4. Make calls to Bitmessage daemon as methods for your object. Examples:

    `$bitmessageObj->newAddress($label, $eighteenByteRipe = false, $totalDifficulty = 1, $smallMessageDifficulty = 1);`
    
    `$bitmessageObj->setStrip(true);`
    
    `$bitmessageObj->broadcast($address, $title, $message);`
    
Contributing
============

You can contribute to this project in different ways:

* Report outstanding issues and bugs by creating an [Issue](https://github.com/Conver/class.bitmessage.php/issues/new)
* Suggest feature enhancements via our [Forum Thread](https://bitmessage.org/forum) on bitmessage forum
* Fork the project, create a branch and file a pull request to improve the code itself

Contact
=======

You can find me on Freenode.net, #MPOS.

Donations
=========

Donations to this project are going directly to [Conver](https://github.com/Conver), the original author of this project:

* LTC address: `---`
* BTC address: `---`

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
