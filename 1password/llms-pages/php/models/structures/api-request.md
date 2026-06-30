# API Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0bSUyRkFQSVJlcXVlc3Q

Represents a request that was made to the API. Including what Token was used and what resource was accessed.

*This model accepts additional fields of type array.*


# Class Name

`ApiRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `action` | [`?string(Action)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/enumerations/action.md) | Optional | - | getAction(): ?string | setAction(?string action): void |
| `actor` | [`?Actor`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/structures/actor.md) | Optional | - | getActor(): ?Actor | setActor(?Actor actor): void |
| `requestId` | `?string` | Optional | The unique id used to identify a single request. | getRequestId(): ?string | setRequestId(?string requestId): void |
| `resource` | [`?Resource2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/structures/resource.md) | Optional | - | getResource(): ?Resource2 | setResource(?Resource2 resource): void |
| `result` | [`?string(Result)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/enumerations/result.md) | Optional | - | getResult(): ?string | setResult(?string result): void |
| `timestamp` | `?DateTime` | Optional, Read-only | The time at which the request was processed by the server. | getTimestamp(): ?\DateTime | setTimestamp(?\DateTime timestamp): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use M1PasswordConnectLib\Models\Builders\ApiRequestBuilder;
use M1PasswordConnectLib\Models\Action;
use M1PasswordConnectLib\Models\Builders\ActorBuilder;
use M1PasswordConnectLib\ApiHelper;
use M1PasswordConnectLib\Models\Builders\Resource2Builder;
use M1PasswordConnectLib\Models\Builders\Item2Builder;
use M1PasswordConnectLib\Models\Type;
use M1PasswordConnectLib\Models\Builders\Vault3Builder;
use M1PasswordConnectLib\Models\Result;

$apiRequest = ApiRequestBuilder::init()
    ->action(Action::READ)
    ->actor(
        ActorBuilder::init()
            ->account('account0')
            ->id('0000193c-0000-0000-0000-000000000000')
            ->jti('jti2')
            ->requestIp('requestIp4')
            ->userAgent('userAgent6')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->requestId('000002a8-0000-0000-0000-000000000000')
    ->resource(
        Resource2Builder::init()
            ->item(
                Item2Builder::init()
                    ->id('id2')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->itemVersion(108)
            ->type(Type::ITEM)
            ->vault(
                Vault3Builder::init()
                    ->id('id6')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->result(Result::SUCCESS)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



