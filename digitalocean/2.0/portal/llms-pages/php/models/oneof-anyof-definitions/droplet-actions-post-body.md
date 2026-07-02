# Droplet Actions Post Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkRyb3BsZXRBY3Rpb25zUG9zdEJvZHk


# Data Type

`V2DropletsActionsRequest|V2DropletsActionsRequest2|V2DropletsActionsRequest21|V2DropletsActionsRequest22|V2DropletsActionsRequest23|V2DropletsActionsRequest24|V2DropletsActionsRequest1`


# Cases

| Type |
|  --- |
| [`V2DropletsActionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-droplets-actions-request.md) |
| [`V2DropletsActionsRequest2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-droplets-actions-request-2.md) |
| [`V2DropletsActionsRequest21`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-droplets-actions-request-21.md) |
| [`V2DropletsActionsRequest22`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-droplets-actions-request-22.md) |
| [`V2DropletsActionsRequest23`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-droplets-actions-request-23.md) |
| [`V2DropletsActionsRequest24`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-droplets-actions-request-24.md) |
| [`V2DropletsActionsRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-droplets-actions-request-1.md) |


# V2DropletsActionsRequest

## Initialization Code

### Example

```php
$value = V2DropletsActionsRequestBuilder::init(
    Type12::REBOOT
)->build();
```


# V2DropletsActionsRequest2

## Initialization Code

### Example

```php
$value = V2DropletsActionsRequest2Builder::init(
    Type12::REBOOT
)
    ->image(12389723)
    ->build();
```


# V2DropletsActionsRequest21

## Initialization Code

### Example

```php
$value = V2DropletsActionsRequest21Builder::init(
    Type12::REBOOT
)
    ->disk(true)
    ->size('s-2vcpu-2gb')
    ->build();
```


# V2DropletsActionsRequest22

## Initialization Code

### Example

```php
$value = V2DropletsActionsRequest22Builder::init(
    Type12::REBOOT
)
    ->image(
        'ubuntu-20-04-x64'
    )
    ->build();
```


# V2DropletsActionsRequest23

## Initialization Code

### Example

```php
$value = V2DropletsActionsRequest23Builder::init(
    Type12::REBOOT
)
    ->name('nifty-new-name')
    ->build();
```


# V2DropletsActionsRequest24

## Initialization Code

### Example

```php
$value = V2DropletsActionsRequest24Builder::init(
    Type12::REBOOT
)
    ->kernel(12389723)
    ->build();
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



