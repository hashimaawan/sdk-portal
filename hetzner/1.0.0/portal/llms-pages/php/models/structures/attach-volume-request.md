# Attach Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkF0dGFjaFZvbHVtZVJlcXVlc3Q

*This model accepts additional fields of type array.*


# Class Name

`AttachVolumeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `automount` | `?bool` | Optional | Auto-mount the Volume after attaching it | getAutomount(): ?bool | setAutomount(?bool automount): void |
| `server` | `int` | Required | ID of the Server the Volume will be attached to | getServer(): int | setServer(int server): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\AttachVolumeRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$attachVolumeRequest = AttachVolumeRequestBuilder::init(
    43
)
    ->automount(false)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



