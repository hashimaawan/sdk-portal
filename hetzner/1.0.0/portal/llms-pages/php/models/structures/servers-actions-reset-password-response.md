# Servers Actions Reset Password Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMFJlc2V0JTI1MjBQYXNzd29yZCUyNTIwUmVzcG9uc2U


# Class Name

`ServersActionsResetPasswordResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `action` | [`?Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action.md) | Optional | - | getAction(): ?Action | setAction(?Action action): void |
| `rootPassword` | `?string` | Optional | Password that will be set for this Server once the Action succeeds | getRootPassword(): ?string | setRootPassword(?string rootPassword): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ServersActionsResetPasswordResponseBuilder;
use HetznerCloudAPILib\Models\Builders\ActionBuilder;
use HetznerCloudAPILib\Models\Builders\Resource2Builder;
use HetznerCloudAPILib\Models\StatusEnum;
use HetznerCloudAPILib\Models\Builders\ErrorBuilder;

$serversActionsResetPasswordResponse = ServersActionsResetPasswordResponseBuilder::init()
    ->action(
        ActionBuilder::init(
            'command6',
            238,
            143.26,
            [
                Resource2Builder::init(
                    198,
                    'type0'
                )->build(),
                Resource2Builder::init(
                    198,
                    'type0'
                )->build(),
                Resource2Builder::init(
                    198,
                    'type0'
                )->build()
            ],
            'started8',
            StatusEnum::RUNNING
        )
            ->error(
                ErrorBuilder::init(
                    'code2',
                    'message4'
                )->build()
            )
            ->finished('finished0')
            ->build()
    )
    ->rootPassword('zCWbFhnu950dUTko5f40')
    ->build();
```



