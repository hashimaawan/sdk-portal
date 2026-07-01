# Create Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZVByaW1hcnlJUFJlcXVlc3Q


# Class Name

`CreatePrimaryIPRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `assigneeId` | `?int` | Optional | ID of the resource the Primary IP should be assigned to. Omitted if it should not be assigned. | getAssigneeId(): ?int | setAssigneeId(?int assigneeId): void |
| `assigneeType` | `string` | Required, Constant | Resource type the Primary IP can be assigned to<br><br>**Value**: `'server'` | getAssigneeType(): string | setAssigneeType(string assigneeType): void |
| `autoDelete` | `?bool` | Optional | Delete the Primary IP when the Server it is assigned to is deleted. If omitted defaults to `false`. | getAutoDelete(): ?bool | setAutoDelete(?bool autoDelete): void |
| `datacenter` | `?string` | Optional | ID or name of Datacenter the Primary IP will be bound to. Needs to be omitted if `assignee_id` is passed. | getDatacenter(): ?string | setDatacenter(?string datacenter): void |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `string` | Required | - | getName(): string | setName(string name): void |
| `type` | [`string(Type51Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-51.md) | Required | Primary IP type | getType(): string | setType(string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\CreatePrimaryIPRequestBuilder;
use HetznerCloudAPILib\Models\Type51Enum;
use HetznerCloudAPILib\ApiHelper;

$createPrimaryIPRequest = CreatePrimaryIPRequestBuilder::init(
    'my-ip',
    Type51Enum::IPV4
)
    ->assigneeId(17)
    ->autoDelete(false)
    ->datacenter('fsn1-dc8')
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->build();
```



