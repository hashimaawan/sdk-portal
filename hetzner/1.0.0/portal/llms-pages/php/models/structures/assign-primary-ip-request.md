# Assign Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkFzc2lnblByaW1hcnlJUFJlcXVlc3Q


# Class Name

`AssignPrimaryIPRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `assigneeId` | `int` | Required | ID of a resource of type `assignee_type` | getAssigneeId(): int | setAssigneeId(int assigneeId): void |
| `assigneeType` | `string` | Required, Constant | Type of resource assigning the Primary IP to<br><br>**Value**: `'server'` | getAssigneeType(): string | setAssigneeType(string assigneeType): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\AssignPrimaryIPRequestBuilder;

$assignPrimaryIPRequest = AssignPrimaryIPRequestBuilder::init(
    4711
)->build();
```



