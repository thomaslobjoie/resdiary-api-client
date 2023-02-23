# Resdiary API Client

Work in progress, do not use yet!

Usage
-----

```php
<?php

use GuzzleHttp\Client;
use Resdiary\ApiClient\Client\GuzzleClient;
use Resdiary\ApiClient\ResdiaryClient;
use Resdiary\ApiClient\ResdiaryMapper;

$client = new ResdiaryClient(
    new GuzzleClient(new Client([
        'base_uri' => 'URL',
        'headers' => [
            'Api-Key' => 'SECRET',
        ],
    ])),
    ResdiaryMapper::create()
);

$client->restaurants()->get(123);
```