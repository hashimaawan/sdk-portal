# Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRk9iamVjdA

Metadata about the Kubernetes API object the diagnostic is reported on.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Object`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `kind` | `?string` | Optional | The kind of Kubernetes API object | getKind(): ?string | setKind(?string kind): void |
| `name` | `?string` | Optional | Name of the object | getName(): ?string | setName(?string name): void |
| `namespace` | `?string` | Optional | The namespace the object resides in the cluster. | getNamespace(): ?string | setNamespace(?string namespace): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\ObjectBuilder;
use DigitalOceanApiLib\ApiHelper;

$object = ObjectBuilder::init()
    ->kind('config map')
    ->name('foo')
    ->namespace('kube-system')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



