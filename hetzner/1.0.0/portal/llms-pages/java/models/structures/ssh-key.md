# Ssh Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNzaEtleQ

*This model accepts additional fields of type Object.*


# Class Name

`SshKey`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) | String getCreated() | setCreated(String created) |
| `Fingerprint` | `String` | Required | Fingerprint of public key | String getFingerprint() | setFingerprint(String fingerprint) |
| `Id` | `int` | Required | ID of the Resource | int getId() | setId(int id) |
| `Labels` | `Map<String, String>` | Required | User-defined labels (key-value pairs) | Map<String, String> getLabels() | setLabels(Map<String, String> labels) |
| `Name` | `String` | Required | Name of the Resource. Must be unique per Project. | String getName() | setName(String name) |
| `PublicKey` | `String` | Required | Public key | String getPublicKey() | setPublicKey(String publicKey) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.SshKey;
import java.io.IOException;
import java.util.LinkedHashMap;

SshKey sshKey = new SshKey.Builder(
    "2016-01-30T23:55:00+00:00",
    "b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f",
    42,
    new LinkedHashMap<String, String>() {{
        put("key0", "labels4");
        put("key1", "labels3");
        put("key2", "labels2");
    }},
    "my-resource",
    "ssh-rsa AAAjjk76kgf...Xt"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



