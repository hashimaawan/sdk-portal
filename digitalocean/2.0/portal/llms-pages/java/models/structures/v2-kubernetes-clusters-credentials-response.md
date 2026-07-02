# V2 Kubernetes Clusters Credentials Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwQ3JlZGVudGlhbHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`V2KubernetesClustersCredentialsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CertificateAuthorityData` | `String` | Optional | A base64 encoding of bytes representing the certificate authority data for accessing the cluster. | String getCertificateAuthorityData() | setCertificateAuthorityData(String certificateAuthorityData) |
| `ClientCertificateData` | `String` | Optional | A base64 encoding of bytes representing the x509 client<br>certificate data for access the cluster. This is only returned for clusters<br>without support for token-based authentication.<br><br>Newly created Kubernetes clusters do not return credentials using<br>certificate-based authentication. For additional information,<br>[see here](https://www.digitalocean.com/docs/kubernetes/how-to/connect-to-cluster/#authenticate). | String getClientCertificateData() | setClientCertificateData(String clientCertificateData) |
| `ClientKeyData` | `String` | Optional | A base64 encoding of bytes representing the x509 client key<br>data for access the cluster. This is only returned for clusters without<br>support for token-based authentication.<br><br>Newly created Kubernetes clusters do not return credentials using<br>certificate-based authentication. For additional information,<br>[see here](https://www.digitalocean.com/docs/kubernetes/how-to/connect-to-cluster/#authenticate). | String getClientKeyData() | setClientKeyData(String clientKeyData) |
| `ExpiresAt` | `LocalDateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the access token expires. | LocalDateTime getExpiresAt() | setExpiresAt(LocalDateTime expiresAt) |
| `Server` | `String` | Optional | The URL used to access the cluster API server. | String getServer() | setServer(String server) |
| `Token` | `String` | Optional | An access token used to authenticate with the cluster. This is only returned for clusters with support for token-based authentication. | String getToken() | setToken(String token) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.V2KubernetesClustersCredentialsResponse;
import java.io.IOException;

V2KubernetesClustersCredentialsResponse v2KubernetesClustersCredentialsResponse = new V2KubernetesClustersCredentialsResponse.Builder()
    .certificateAuthorityData("LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSURKekNDQWcrZ0F3SUJBZ0lDQm5Vd0RRWUpLb1pJaHZjTkFRRUxCUUF3TXpFVk1CTUdBMVVFQ2hNTVJHbG4KYVhSaGJFOWpaV0Z1TVJvd0dBWURWUVFERXhGck9ITmhZWE1nUTJ4MWMzUmxjaUJEUVRBZUZ3MHlNREE0TURNeApOVEkxTWpoYUZ3MDBNREE0TURNeE5USTFNamhhTURNeEZUQVRCZ05WQkFvVERFUnBaMmwwWVd4UFkyVmhiakVhCk1CZ0dBMVVFQXhNUmF6aHpZV0Z6SUVOc2RYTjBaWElnUTBFd2dnRWlNQTBHQ1NxR1NJYjNEUUVCQVFVQUE0SUIKRHdBd2dnRUtBb0lCQVFDc21oa2JrSEpUcGhZQlN0R05VVE1ORVZTd2N3bmRtajArelQvcUZaNGsrOVNxUnYrSgpBd0lCaGpBU0JnTlZIUk1CQWY4RUNEQUdBUUgvQWdFQU1CMEdBMVVkRGdRV0JCUlRzazhhZ1hCUnFyZXdlTXJxClhwa3E1NXg5dVRBTkJna3Foa2lHOXcwQkFRc0ZBQU9DQVFFQXB6V2F6bXNqYWxXTEx3ZjVpbWdDblNINDlKcGkKYWkvbzFMdEJvVEpleGdqZzE1ZVppaG5BMUJMc0lWNE9BZGM3UEFsL040L0hlbENrTDVxandjamRnNVdaYnMzYwozcFVUQ0g5bVVwMFg1SVdhT1VKV292Q1hGUlM1R2VKYXlkSDVPUXhqTURzR2N2UlNvZGQrVnQ2MXE3aWdFZ2I1CjBOZ1l5RnRnc2p0MHpJN3hURzZFNnlsOVYvUmFoS3lIQks2eExlM1RnUGU4SXhWa2RwT3QzR0FhSDRaK0pLR3gKYisyMVZia1NnRE1QQTlyR0VKNVZwVXlBV0FEVXZDRVFHV0hmNGpQN2ZGZlc3T050S0JWY3h3YWFjcVBVdUhzWApwRG5DZVR3V1NuUVp6L05xNmQxWUtsMFdtbkwzTEowemJzRVFGbEQ4MkkwL09MY2dZSDVxMklOZHhBPT0KLS0tLS1FTkQgQ0VSVElGSUNBVEUtLS0tLQo=")
    .clientCertificateData("client_certificate_data0")
    .clientKeyData("client_key_data4")
    .expiresAt(DateTimeHelper.fromRfc8601DateTime("2019-11-09T11:50:28.889080521Z"))
    .server("https://bd5f5959-5e1e-4205-a714-a914373942af.k8s.ondigitalocean.com")
    .token("$DIGITALOCEAN_TOKEN")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



