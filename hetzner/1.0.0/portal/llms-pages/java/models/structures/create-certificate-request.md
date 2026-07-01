# Create Certificate Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZUNlcnRpZmljYXRlUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`CreateCertificateRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Certificate` | `String` | Optional | Certificate and chain in PEM format, in order so that each record directly certifies the one preceding. Required for type `uploaded` Certificates. | String getCertificate() | setCertificate(String certificate) |
| `DomainNames` | `List<String>` | Optional | Domains and subdomains that should be contained in the Certificate issued by *Let's Encrypt*. Required for type `managed` Certificates. | List<String> getDomainNames() | setDomainNames(List<String> domainNames) |
| `Labels` | `Object` | Optional | User-defined labels (key-value pairs) | Object getLabels() | setLabels(Object labels) |
| `Name` | `String` | Required | Name of the Certificate | String getName() | setName(String name) |
| `PrivateKey` | `String` | Optional | Certificate key in PEM format. Required for type `uploaded` Certificates. | String getPrivateKey() | setPrivateKey(String privateKey) |
| `Type` | [`Type1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-1.md) | Optional | Choose between uploading a Certificate in PEM format or requesting a managed *Let's Encrypt* Certificate. If omitted defaults to `uploaded`. | Type1 getType() | setType(Type1 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.CreateCertificateRequest;
import cloud.hetzner.api.models.Type1;
import java.io.IOException;
import java.util.Arrays;

CreateCertificateRequest createCertificateRequest = new CreateCertificateRequest.Builder(
    "my website cert"
)
.certificate("-----BEGIN CERTIFICATE-----\n...")
.domainNames(Arrays.asList(
        "domain_names8",
        "domain_names9",
        "domain_names0"
    ))
.labels(ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.privateKey("-----BEGIN PRIVATE KEY-----\n...")
.type(Type1.UPLOADED)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



