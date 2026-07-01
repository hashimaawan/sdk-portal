# Get Quotes for All Symbols

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/#/php/x-redirect/JTI0ZSUyRmZvcmV4JTJGR2V0JTI1MjBxdW90ZXMlMjUyMGZvciUyNTIwYWxsJTI1MjBzeW1ib2xz

Get quotes

Find out more: [http://1forge.com/forex-data-api](http://1forge.com/forex-data-api)

:information_source: **Note** This endpoint does not require authentication.

```php
function getQuotesForAllSymbols(): void
```


# Response Type

**200**: A list of quotes

`void`


# Example Usage

```php
$forexController = $client->getForexController();

try {
    $forexController->getQuotesForAllSymbols();
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```



