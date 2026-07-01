# Get a List of Symbols for Which We Provide Real-Time Quotes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/#/php/x-redirect/JTI0ZSUyRmZvcmV4JTJGR2V0JTI1MjBhJTI1MjBsaXN0JTI1MjBvZiUyNTIwc3ltYm9scyUyNTIwZm9yJTI1MjB3aGljaCUyNTIwd2UlMjUyMHByb3ZpZGUlMjUyMHJlYWwtdGltZSUyNTIwcXVvdGVz

Symbol List

Find out more: [http://1forge.com/forex-data-api](http://1forge.com/forex-data-api)

:information_source: **Note** This endpoint does not require authentication.

```php
function getAListOfSymbolsForWhichWeProvideRealTimeQuotes(): array
```


# Response Type

**200**: A list of symbols

`string[]`


# Example Usage

```php
$forexController = $client->getForexController();

try {
    $result = $forexController->getAListOfSymbolsForWhichWeProvideRealTimeQuotes();
    echo 'string[]:';
    var_dump($result);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```



