# Servers Actions Enable Rescue Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEVuYWJsZSUyNTIwUmVzY3VlJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`ServersActionsEnableRescueRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SshKeys` | `List<Integer>` | Optional | Array of SSH key IDs which should be injected into the rescue system. | List<Integer> getSshKeys() | setSshKeys(List<Integer> sshKeys) |
| `Type` | [`Type65`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-65.md) | Optional | Type of rescue system to boot (default: `linux64`) | Type65 getType() | setType(Type65 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.ServersActionsEnableRescueRequest;
import cloud.hetzner.api.models.Type65;
import java.io.IOException;
import java.util.Arrays;

ServersActionsEnableRescueRequest serversActionsEnableRescueRequest = new ServersActionsEnableRescueRequest.Builder()
    .sshKeys(Arrays.asList(
        2323
    ))
    .type(Type65.LINUX64)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



