# Floating Ips Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMEFjdGlvbnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type array.*


# Class Name

`FloatingIpsActionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `actions` | [`Action[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action.md) | Required | - | getActions(): array | setActions(array actions): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\FloatingIpsActionsResponseBuilder;
use HetznerCloudApiLib\Models\Builders\ActionBuilder;
use HetznerCloudApiLib\Models\Builders\Resource2Builder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Status;
use HetznerCloudApiLib\Models\Builders\ErrorBuilder;

$floatingIpsActionsResponse = FloatingIpsActionsResponseBuilder::init(
    [
        ActionBuilder::init(
            'start_server',
            42,
            100,
            [
                Resource2Builder::init(
                    42,
                    'server'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ],
            '2016-01-30T23:55:00+00:00',
            Status::SUCCESS
        )
            ->error(
                ErrorBuilder::init(
                    'action_failed',
                    'Action failed'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->finished('2016-01-30T23:55:00+00:00')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ]
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



