# Env

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkVudg

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Env`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Key` | `string` | Required | The variable name<br><br>**Constraints**: *Pattern*: `^[_A-Za-z][_A-Za-z0-9]*$` |
| `Scope` | [`*models.Scope`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/scope.md) | Optional | - RUN_TIME: Made available only at run-time<br>- BUILD_TIME: Made available only at build-time<br>- RUN_AND_BUILD_TIME: Made available at both build and run-time<br><br>**Default**: `"RUN_AND_BUILD_TIME"` |
| `Type` | [`*models.Type2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/type-2.md) | Optional | - GENERAL: A plain-text environment variable<br>- SECRET: A secret encrypted environment variable<br><br>**Default**: `"GENERAL"` |
| `Value` | `*string` | Optional | The value. If the type is `SECRET`, the value will be encrypted on first submission. On following submissions, the encrypted value should be used. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    env := models.Env{
        Key:                   "BASE_URL",
        Scope:                 models.ToPointer(models.Scope_BuildTime),
        Type:                  models.ToPointer(models.Type2_General),
        Value:                 models.ToPointer("http://example.com"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



