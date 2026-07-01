# Servers Actions Enable Rescue Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEVuYWJsZSUyNTIwUmVzY3VlJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type array.*


# Class Name

`ServersActionsEnableRescueRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `sshKeys` | `?(int[])` | Optional | Array of SSH key IDs which should be injected into the rescue system. | getSshKeys(): ?array | setSshKeys(?array sshKeys): void |
| `type` | [`?string(Type65)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-65.md) | Optional | Type of rescue system to boot (default: `linux64`) | getType(): ?string | setType(?string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ServersActionsEnableRescueRequestBuilder;
use HetznerCloudApiLib\Models\Type65;
use HetznerCloudApiLib\ApiHelper;

$serversActionsEnableRescueRequest = ServersActionsEnableRescueRequestBuilder::init()
    ->sshKeys(
        [
            2323
        ]
    )
    ->type(Type65::LINUX64)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



