# Account

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkFjY291bnQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Account`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dropletLimit` | `int` | Required | The total number of Droplets current user or team may have active at one time. | getDropletLimit(): int | setDropletLimit(int dropletLimit): void |
| `email` | `string` | Required | The email address used by the current user to register for DigitalOcean. | getEmail(): string | setEmail(string email): void |
| `emailVerified` | `bool` | Required | If true, the user has verified their account via email. False otherwise.<br><br>**Default**: `false` | getEmailVerified(): bool | setEmailVerified(bool emailVerified): void |
| `floatingIpLimit` | `int` | Required | The total number of Floating IPs the current user or team may have. | getFloatingIpLimit(): int | setFloatingIpLimit(int floatingIpLimit): void |
| `status` | [`string(Status)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/status.md) | Required | This value is one of "active", "warning" or "locked".<br><br>**Default**: `Status::ACTIVE` | getStatus(): string | setStatus(string status): void |
| `statusMessage` | `string` | Required | A human-readable message giving more details about the status of the account. | getStatusMessage(): string | setStatusMessage(string statusMessage): void |
| `team` | [`?Team`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/team.md) | Optional | When authorized in a team context, includes information about the current team. | getTeam(): ?Team | setTeam(?Team team): void |
| `uuid` | `string` | Required | The unique universal identifier for the current user. | getUuid(): string | setUuid(string uuid): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\AccountBuilder;
use DigitalOceanApiLib\Models\Status;
use DigitalOceanApiLib\Models\Builders\TeamBuilder;
use DigitalOceanApiLib\ApiHelper;

$account = AccountBuilder::init(
    25,
    'sammy@digitalocean.com',
    true,
    5,
    Status::ACTIVE,
    ' ',
    'b6fr89dbf6d9156cace5f3c78dc9851d957381ef'
)
    ->team(
        TeamBuilder::init()
            ->name('name0')
            ->uuid('uuid6')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



