# Env

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkVudg

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Env`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Key` | `string` | Required | The variable name<br><br>**Constraints**: *Pattern*: `^[_A-Za-z][_A-Za-z0-9]*$` |
| `Scope` | [`Scope?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/scope.md) | Optional | - RUN_TIME: Made available only at run-time<br>- BUILD_TIME: Made available only at build-time<br>- RUN_AND_BUILD_TIME: Made available at both build and run-time<br><br>**Default**: `Scope.RUN_AND_BUILD_TIME` |
| `Type` | [`Type2?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/type-2.md) | Optional | - GENERAL: A plain-text environment variable<br>- SECRET: A secret encrypted environment variable<br><br>**Default**: `Type2.GENERAL` |
| `MValue` | `string` | Optional | The value. If the type is `SECRET`, the value will be encrypted on first submission. On following submissions, the encrypted value should be used. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Env env = new Env
{
    Key = "BASE_URL",
    Scope = Scope.BuildTime,
    Type = Type2.General,
    MValue = "http://example.com",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



