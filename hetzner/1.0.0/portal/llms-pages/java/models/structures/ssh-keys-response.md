# Ssh Keys Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVzcG9uc2U


# Class Name

`SshKeysResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/meta.md) | Optional | - | Meta getMeta() | setMeta(Meta meta) |
| `SshKeys` | [`List<SshKey>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/ssh-key.md) | Required | - | List<SshKey> getSshKeys() | setSshKeys(List<SshKey> sshKeys) |


# Example

```java
import cloud.hetzner.api.models.Meta;
import cloud.hetzner.api.models.Pagination;
import cloud.hetzner.api.models.SshKey;
import cloud.hetzner.api.models.SshKeysResponse;
import java.util.Arrays;
import java.util.LinkedHashMap;

SshKeysResponse sshKeysResponse = new SshKeysResponse.Builder(
    Arrays.asList(
        new SshKey.Builder(
            "2016-01-30T23:55:00+00:00",
            "b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f",
            42,
            new LinkedHashMap<String, String>() {{
                put("key0", "labels4");
                put("key1", "labels5");
                put("key2", "labels6");
            }},
            "my-resource",
            "ssh-rsa AAAjjk76kgf...Xt"
        )
        .build()
    )
)
.meta(new Meta.Builder(
        new Pagination.Builder(
            77.7D,
            209.18D,
            17.58D,
            13.34D,
            50.02D,
            206.64D
        )
        .build()
    )
    .build())
.build();
```



