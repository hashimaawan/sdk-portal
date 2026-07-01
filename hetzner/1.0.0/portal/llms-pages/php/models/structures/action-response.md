# Action Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkFjdGlvblJlc3BvbnNl


# Class Name

`ActionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action.md) | Required | - | getAction(): Action | setAction(Action action): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ActionResponseBuilder;
use HetznerCloudAPILib\Models\Builders\ActionBuilder;
use HetznerCloudAPILib\Models\Builders\Resource2Builder;
use HetznerCloudAPILib\Models\StatusEnum;
use HetznerCloudAPILib\Models\Builders\ErrorBuilder;

$actionResponse = ActionResponseBuilder::init(
    ActionBuilder::init(
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
        ->build()
)->build();
```



