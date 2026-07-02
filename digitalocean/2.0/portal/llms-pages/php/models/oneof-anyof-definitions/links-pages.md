# Links Pages

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkxpbmtzUGFnZXM


# Data Type

`Pages|Pages1|array`


# Cases

| Type |
|  --- |
| [`Pages`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/pages.md) |
| [`Pages1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/pages-1.md) |
| [`array`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) |


# Pages

## Initialization Code

### Example

```php
$value = PagesBuilder::init()
    ->last('https://api.digitalocean.com/v2/images?page=2')
    ->next('https://api.digitalocean.com/v2/images?page=2')
    ->build();
```


# Pages1

## Initialization Code

### Example

```php
$value = Pages1Builder::init()
    ->first('https://api.digitalocean.com/v2/images?page=1')
    ->prev('https://api.digitalocean.com/v2/images?page=1')
    ->build();
```


# array

## Initialization Code

### Example

```php
$value = ApiHelper::deserialize('{"key1":"val1","key2":"val2"}');
```



