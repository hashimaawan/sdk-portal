# Ssh Keys Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVzcG9uc2Ux


# Class Name

`SshKeysResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SshKey` | [`SshKey`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/ssh-key.md) | Required | - | SshKey getSshKey() | setSshKey(SshKey sshKey) |


# Example

```java
import cloud.hetzner.api.models.SshKey;
import cloud.hetzner.api.models.SshKeysResponse1;
import java.util.LinkedHashMap;

SshKeysResponse1 sshKeysResponse1 = new SshKeysResponse1.Builder(
    new SshKey.Builder(
        "2016-01-30T23:55:00+00:00",
        "b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f",
        42,
        new LinkedHashMap<String, String>() {{
            put("key0", "labels0");
        }},
        "my-resource",
        "ssh-rsa AAAjjk76kgf...Xt"
    )
    .build()
)
.build();
```



