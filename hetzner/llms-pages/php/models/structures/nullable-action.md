# Nullable Action

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRk51bGxhYmxlQWN0aW9u


# Class Name

`NullableAction`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `command` | `string` | Required | Command executed in the Action | getCommand(): string | setCommand(string command): void |
| `error` | [`?Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/error.md) | Required | Error message for the Action if error occurred, otherwise null | getError(): ?Error | setError(?Error error): void |
| `finished` | `?string` | Required | Point in time when the Action was finished (in ISO-8601 format). Only set if the Action is finished otherwise null. | getFinished(): ?string | setFinished(?string finished): void |
| `id` | `int` | Required | ID of the Resource | getId(): int | setId(int id): void |
| `progress` | `float` | Required | Progress of Action in percent | getProgress(): float | setProgress(float progress): void |
| `resources` | [`Resource2[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/resource.md) | Required | Resources the Action relates to | getResources(): array | setResources(array resources): void |
| `started` | `string` | Required | Point in time when the Action was started (in ISO-8601 format) | getStarted(): string | setStarted(string started): void |
| `status` | [`string(StatusEnum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/status.md) | Required | Status of the Action | getStatus(): string | setStatus(string status): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\NullableActionBuilder;
use HetznerCloudAPILib\Models\Builders\Resource2Builder;
use HetznerCloudAPILib\Models\StatusEnum;
use HetznerCloudAPILib\Models\Builders\ErrorBuilder;

$nullableAction = NullableActionBuilder::init(
    'start_server',
    42,
    100,
    [
        Resource2Builder::init(
            42,
            'server'
        )->build()
    ],
    '2016-01-30T23:55:00+00:00',
    StatusEnum::RUNNING
)
    ->error(
        ErrorBuilder::init(
            'action_failed',
            'Action failed'
        )->build()
    )
    ->finished('2016-01-30T23:55:00+00:00')
    ->build();
```



