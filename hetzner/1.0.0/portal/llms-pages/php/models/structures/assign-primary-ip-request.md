# Assign Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkFzc2lnblByaW1hcnlJUFJlcXVlc3Q

*This model accepts additional fields of type array.*


# Class Name

`AssignPrimaryIpRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `assigneeId` | `int` | Required | ID of a resource of type `assignee_type` | getAssigneeId(): int | setAssigneeId(int assigneeId): void |
| `assigneeType` | `string` | Required, Constant | Type of resource assigning the Primary IP to<br><br>**Value**: `'server'` | getAssigneeType(): string | setAssigneeType(string assigneeType): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\AssignPrimaryIpRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$assignPrimaryIpRequest = AssignPrimaryIpRequestBuilder::init(
    4711
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



