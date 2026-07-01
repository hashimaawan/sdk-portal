# Create Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZVByaW1hcnlJUFJlcXVlc3Q

*This model accepts additional fields of type array.*


# Class Name

`CreatePrimaryIpRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `assigneeId` | `?int` | Optional | ID of the resource the Primary IP should be assigned to. Omitted if it should not be assigned. | getAssigneeId(): ?int | setAssigneeId(?int assigneeId): void |
| `assigneeType` | `string` | Required, Constant | Resource type the Primary IP can be assigned to<br><br>**Value**: `'server'` | getAssigneeType(): string | setAssigneeType(string assigneeType): void |
| `autoDelete` | `?bool` | Optional | Delete the Primary IP when the Server it is assigned to is deleted. If omitted defaults to `false`. | getAutoDelete(): ?bool | setAutoDelete(?bool autoDelete): void |
| `datacenter` | `?string` | Optional | ID or name of Datacenter the Primary IP will be bound to. Needs to be omitted if `assignee_id` is passed. | getDatacenter(): ?string | setDatacenter(?string datacenter): void |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `string` | Required | - | getName(): string | setName(string name): void |
| `type` | [`string(Type51)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-51.md) | Required | Primary IP type | getType(): string | setType(string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\CreatePrimaryIpRequestBuilder;
use HetznerCloudApiLib\Models\Type51;
use HetznerCloudApiLib\ApiHelper;

$createPrimaryIpRequest = CreatePrimaryIpRequestBuilder::init(
    'my-ip',
    Type51::IPV4
)
    ->assigneeId(17)
    ->autoDelete(false)
    ->datacenter('fsn1-dc8')
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



