# Ssh Keys Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVxdWVzdA


# Class Name

`SshKeysRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Labels` | `Object` | Optional | User-defined labels (key-value pairs) | Object getLabels() | setLabels(Object labels) |
| `Name` | `String` | Required | Name of the SSH key | String getName() | setName(String name) |
| `PublicKey` | `String` | Required | Public key | String getPublicKey() | setPublicKey(String publicKey) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.SshKeysRequest;
import java.io.IOException;

SshKeysRequest sshKeysRequest = new SshKeysRequest.Builder(
    "My ssh key",
    "ssh-rsa AAAjjk76kgf...Xt"
)
.labels(ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



