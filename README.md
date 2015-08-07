PHP SDK for Botan.io
================

Installation
------------
To get started, get [Composer](http://getcomposer.org/download/).

 Run:
 ```
 $ php composer.phar require IPRIT/botan-php:*
 ```
 or add
 ```
 "IPRIT/botan-php": "*"
 ```
 to the `require` section of your `composer.json` file.


Usage
-----
0. Now you can use wrapper
Create [Yandex.AppMetrica](https://appmetrica.yandex.com/) api token and insert into $token variable.
 ```php
 private $token = 'token';

 public function _incomingMessage($message_json) {
     $messageObj = json_decode($message_json, true);
     $messageData = $messageObj['message'];

     $botan = new IPRIT\BotanSDK\Botan($this->token);
     $botan->track($messageData, 'Start');
 }
 ```