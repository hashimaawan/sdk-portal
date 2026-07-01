# Servers Actions Enable Rescue Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEVuYWJsZSUyNTIwUmVzY3VlJTI1MjBSZXF1ZXN0


# Class Name

`ServersActionsEnableRescueRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SshKeys` | `List<Integer>` | Optional | Array of SSH key IDs which should be injected into the rescue system. | List<Integer> getSshKeys() | setSshKeys(List<Integer> sshKeys) |
| `Type` | [`Type65Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-65.md) | Optional | Type of rescue system to boot (default: `linux64`) | Type65Enum getType() | setType(Type65Enum type) |


# Example

```java
import cloud.hetzner.api.models.ServersActionsEnableRescueRequest;
import cloud.hetzner.api.models.Type65Enum;
import java.util.Arrays;

ServersActionsEnableRescueRequest serversActionsEnableRescueRequest = new ServersActionsEnableRescueRequest.Builder()
    .sshKeys(Arrays.asList(
        2323
    ))
    .type(Type65Enum.LINUX64)
    .build();
```



