# Droplet Actions Post by Tag Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkRyb3BsZXRBY3Rpb25zUG9zdEJ5VGFnQm9keQ


# Data Type

`V2DropletsActionsRequest|V2DropletsActionsRequest1`


# Cases

| Type |
|  --- |
| [`V2DropletsActionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-droplets-actions-request.md) |
| [`V2DropletsActionsRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-droplets-actions-request-1.md) |


# V2DropletsActionsRequest

## Initialization Code

### Example

```php
$value = V2DropletsActionsRequestBuilder::init(
    Type12::REBOOT
)->build();
```


# V2DropletsActionsRequest1

## Initialization Code

### Example

```php
$value = V2DropletsActionsRequest1Builder::init(
    Type12::REBOOT
)
    ->name('Nifty New Snapshot')
    ->build();
```



