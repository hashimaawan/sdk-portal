# Contains All Domains for the App

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkNvbnRhaW5zJTI1MjBhbGwlMjUyMGRvbWFpbnMlMjUyMGZvciUyNTIwdGhlJTI1MjBhcHA

*This model accepts additional fields of type Object.*


# Class Name

`ContainsAllDomainsForTheApp`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CertificateExpiresAt` | `LocalDateTime` | Optional, Read-only | - | LocalDateTime getCertificateExpiresAt() | setCertificateExpiresAt(LocalDateTime certificateExpiresAt) |
| `Id` | `String` | Optional | - | String getId() | setId(String id) |
| `Phase` | [`Phase1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/phase-1.md) | Optional | **Default**: `Phase1.UNKNOWN` | Phase1 getPhase() | setPhase(Phase1 phase) |
| `Progress` | [`Progress1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/progress-1.md) | Optional | - | Progress1 getProgress() | setProgress(Progress1 progress) |
| `RotateValidationRecords` | `Boolean` | Optional, Read-only | - | Boolean getRotateValidationRecords() | setRotateValidationRecords(Boolean rotateValidationRecords) |
| `Spec` | [`Domain`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/domain.md) | Optional | - | Domain getSpec() | setSpec(Domain spec) |
| `Validations` | [`List<ListOfTxtValidationRecord>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/list-of-txt-validation-record.md) | Optional | - | List<ListOfTxtValidationRecord> getValidations() | setValidations(List<ListOfTxtValidationRecord> validations) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.ContainsAllDomainsForTheApp;
import com.digitalocean.api.models.Phase1;
import com.digitalocean.api.models.Progress1;
import java.io.IOException;
import java.util.Arrays;

ContainsAllDomainsForTheApp containsAllDomainsForTheApp = new ContainsAllDomainsForTheApp.Builder()
    .certificateExpiresAt(DateTimeHelper.fromRfc8601DateTime("2024-01-29T23:59:59Z"))
    .id("4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf")
    .phase(Phase1.ACTIVE)
    .progress(new Progress1.Builder()
        .steps(Arrays.asList(
            ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}")
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .rotateValidationRecords(false)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



