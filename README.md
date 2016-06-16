# PHP Wraper for BMTC API


Bangalore Metropolitan Transport Corporation BMTC recently released its Intelligent Transport System (ITS) , But as of now there is no official public api available. This is an approch to build a php wraper based on the Reverse engineering work done by [**Aboobacker MK.**](https://github.com/tachyons)

API Reference : https://github.com/tachyons/bmtc_api

## Installation
First enable php-curl extension in apache.

If you are in ubuntu 16.04, type
```bash
sudo apt-get install php-curl
```

Then add this line to the top of your php application

```php
require 'bmct.php';
```

## Usage

Create a new instance.

```php
$bmct = new Bmct();
```

Route wise details.

```php
$result = $bmct->route_wise('direction', '<routeNo>');
```

Route map details.
```php
$result = $bmct->route_map('<direction>', '<routeNo>');
```
Nearest stop details.

```php
$result = $bmct->nearest_stop('<lattitude>', '<longitude>');
```
Get stops matching the query string.

```php
$result = $bmct->search_stop('<keyword>');
```
Get stop details based on Stop ID.

```php
$result = $bmct->stop_details('<stopId>');
```
Note: Every methods described above either returns an array of objects or a NULL array.

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/tvsijin/bmtc-api-php. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.


## License

This repository is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

## Demo

@TODO
