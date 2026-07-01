# Servers Actions Request Console Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMFJlcXVlc3QlMjUyMENvbnNvbGUlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type array.*


# Class Name

`ServersActionsRequestConsoleResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action.md) | Required | - | getAction(): Action | setAction(Action action): void |
| `password` | `string` | Required | VNC password to use for this connection (this password only works in combination with a wss_url with valid token) | getPassword(): string | setPassword(string password): void |
| `wssUrl` | `string` | Required | URL of websocket proxy to use; this includes a token which is valid for a limited time only | getWssUrl(): string | setWssUrl(string wssUrl): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ServersActionsRequestConsoleResponseBuilder;
use HetznerCloudApiLib\Models\Builders\ActionBuilder;
use HetznerCloudApiLib\Models\Builders\Resource2Builder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Status;
use HetznerCloudApiLib\Models\Builders\ErrorBuilder;

$serversActionsRequestConsoleResponse = ServersActionsRequestConsoleResponseBuilder::init(
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
        Status::RUNNING
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
        ->build(),
    '9MQaTg2VAGI0FIpc10k3UpRXcHj2wQ6x',
    'wss://console.hetzner.cloud/?server_id=1&token=3db32d15-af2f-459c-8bf8-dee1fd05f49c'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



