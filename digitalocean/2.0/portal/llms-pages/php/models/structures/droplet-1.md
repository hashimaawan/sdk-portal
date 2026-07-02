# Droplet 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkRyb3BsZXQx

An object containing information about a resource scheduled for deletion.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Droplet1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `destroyedAt` | `?DateTime` | Optional | A time value given in ISO8601 combined date and time format indicating when the resource was destroyed if the request was successful. | getDestroyedAt(): ?\DateTime | setDestroyedAt(?\DateTime destroyedAt): void |
| `errorMessage` | `?string` | Optional | A string indicating that the resource was not successfully destroyed and providing additional information. | getErrorMessage(): ?string | setErrorMessage(?string errorMessage): void |
| `id` | `?string` | Optional | The unique identifier for the resource scheduled for deletion. | getId(): ?string | setId(?string id): void |
| `name` | `?string` | Optional | The name of the resource scheduled for deletion. | getName(): ?string | setName(?string name): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Droplet1Builder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\ApiHelper;

$droplet1 = Droplet1Builder::init()
    ->destroyedAt(DateTimeHelper::fromRfc3339DateTime('2020-04-01T18:11:49Z'))
    ->errorMessage('error_message0')
    ->id('61486916')
    ->name('ubuntu-s-1vcpu-1gb-nyc1-01-1585758823330')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



