# V2 Kubernetes Clusters Clusterlint Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwQ2x1c3RlcmxpbnQlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2KubernetesClustersClusterlintResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `completedAt` | `?DateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the schedule clusterlint run request was completed. | getCompletedAt(): ?\DateTime | setCompletedAt(?\DateTime completedAt): void |
| `diagnostics` | [`?(Diagnostic[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/diagnostic.md) | Optional | An array of diagnostics reporting potential problems for the given cluster. | getDiagnostics(): ?array | setDiagnostics(?array diagnostics): void |
| `requestedAt` | `?DateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the schedule clusterlint run request was made. | getRequestedAt(): ?\DateTime | setRequestedAt(?\DateTime requestedAt): void |
| `runId` | `?string` | Optional | Id of the clusterlint run that can be used later to fetch the diagnostics. | getRunId(): ?string | setRunId(?string runId): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2KubernetesClustersClusterlintResponseBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\DiagnosticBuilder;
use DigitalOceanApiLib\Models\Builders\ObjectBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2KubernetesClustersClusterlintResponse = V2KubernetesClustersClusterlintResponseBuilder::init()
    ->completedAt(DateTimeHelper::fromRfc3339DateTime('2019-10-30T05:34:11Z'))
    ->diagnostics(
        [
            DiagnosticBuilder::init()
                ->checkName('check_name8')
                ->message('message2')
                ->object(
                    ObjectBuilder::init()
                        ->kind('kind0')
                        ->name('name2')
                        ->namespace('namespace0')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->severity('severity2')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            DiagnosticBuilder::init()
                ->checkName('check_name8')
                ->message('message2')
                ->object(
                    ObjectBuilder::init()
                        ->kind('kind0')
                        ->name('name2')
                        ->namespace('namespace0')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->severity('severity2')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->requestedAt(DateTimeHelper::fromRfc3339DateTime('2019-10-30T05:34:07Z'))
    ->runId('50c2f44c-011d-493e-aee5-361a4a0d1844')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



