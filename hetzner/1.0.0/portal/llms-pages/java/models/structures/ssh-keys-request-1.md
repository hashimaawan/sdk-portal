# Ssh Keys Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVxdWVzdDE


# Class Name

`SshKeysRequest1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Labels` | `Object` | Optional | User-defined labels (key-value pairs) | Object getLabels() | setLabels(Object labels) |
| `Name` | `String` | Optional | New name Name to set | String getName() | setName(String name) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.SshKeysRequest1;
import java.io.IOException;

SshKeysRequest1 sshKeysRequest1 = new SshKeysRequest1.Builder()
    .labels(ApiHelper.deserialize("{\"labelkey\":\"value\"}"))
    .name("My ssh key")
    .build();
```



