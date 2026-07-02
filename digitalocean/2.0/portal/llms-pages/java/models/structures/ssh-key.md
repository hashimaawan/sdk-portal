# Ssh Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlNzaEtleQ

*This model accepts additional fields of type Object.*


# Class Name

`SshKey`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Fingerprint` | `String` | Optional, Read-only | A unique identifier that differentiates this key from other keys using  a format that SSH recognizes. The fingerprint is created when the key is added to your account. | String getFingerprint() | setFingerprint(String fingerprint) |
| `Id` | `Integer` | Optional, Read-only | A unique identification number for this key. Can be used to embed a  specific SSH key into a Droplet. | Integer getId() | setId(Integer id) |
| `Name` | `String` | Required | A human-readable display name for this key, used to easily identify the SSH keys when they are displayed. | String getName() | setName(String name) |
| `PublicKey` | `String` | Required | The entire public key string that was uploaded. Embedded into the root user's `authorized_keys` file if you include this key during Droplet creation. | String getPublicKey() | setPublicKey(String publicKey) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.SshKey;
import java.io.IOException;

SshKey sshKey = new SshKey.Builder(
    "My SSH Public Key",
    "ssh-rsa AEXAMPLEaC1yc2EAAAADAQABAAAAQQDDHr/jh2Jy4yALcK4JyWbVkPRaWmhck3IgCoeOO3z1e2dBowLh64QAM+Qb72pxekALga2oi4GvT+TlWNhzPH4V example"
)
.fingerprint("3b:16:bf:e4:8b:00:8b:b8:59:8c:a9:d3:f0:19:45:fa")
.id(512189)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



