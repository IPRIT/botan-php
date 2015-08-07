PHP SDK for Botan.io
================

Installation
------------
To get started, get [Composer](http://getcomposer.org/download/).

 Run:
 ```
 $ php composer.phar require iprit/botan-php:*
 ```
 or add
 ```
 "iprit/botan-php": "*"
 ```
 to the `require` section of your `composer.json` file.


Usage
-----
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