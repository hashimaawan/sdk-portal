# Servers Actions Attach Iso Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEF0dGFjaCUyNTIwSXNvJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type array.*


# Class Name

`ServersActionsAttachIsoRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `iso` | `string` | Required | ID or name of ISO to attach to the Server as listed in GET `/isos` | getIso(): string | setIso(string iso): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ServersActionsAttachIsoRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$serversActionsAttachIsoRequest = ServersActionsAttachIsoRequestBuilder::init(
    'FreeBSD-11.0-RELEASE-amd64-dvd1'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



