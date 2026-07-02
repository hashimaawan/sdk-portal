# V2 Projects Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`V2ProjectsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CreatedAt` | `LocalDateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the project was created. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `Description` | `String` | Optional | The description of the project. The maximum length is 255 characters.<br><br>**Constraints**: *Maximum Length*: `255` | String getDescription() | setDescription(String description) |
| `Environment` | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/environment.md) | Optional | The environment of the project's resources. | Environment getEnvironment() | setEnvironment(Environment environment) |
| `Id` | `UUID` | Optional, Read-only | The unique universal identifier of this project. | UUID getId() | setId(UUID id) |
| `Name` | `String` | Optional | The human-readable name for the project. The maximum length is 175 characters and the name must be unique.<br><br>**Constraints**: *Maximum Length*: `175` | String getName() | setName(String name) |
| `OwnerId` | `Integer` | Optional, Read-only | The integer id of the project owner. | Integer getOwnerId() | setOwnerId(Integer ownerId) |
| `OwnerUuid` | `String` | Optional, Read-only | The unique universal identifier of the project owner. | String getOwnerUuid() | setOwnerUuid(String ownerUuid) |
| `Purpose` | `String` | Optional | The purpose of the project. The maximum length is 255 characters. It can<br>have one of the following values:<br><br>- Just trying out DigitalOcean<br>- Class project / Educational purposes<br>- Website or blog<br>- Web Application<br>- Service or API<br>- Mobile Application<br>- Machine learning / AI / Data processing<br>- IoT<br>- Operational / Developer tooling<br><br>If another value for purpose is specified, for example, "your custom purpose",<br>your purpose will be stored as `Other: your custom purpose`.<br><br>**Constraints**: *Maximum Length*: `255` | String getPurpose() | setPurpose(String purpose) |
| `UpdatedAt` | `LocalDateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the project was updated. | LocalDateTime getUpdatedAt() | setUpdatedAt(LocalDateTime updatedAt) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Environment;
import com.digitalocean.api.models.V2ProjectsRequest;
import java.io.IOException;
import java.util.UUID;

V2ProjectsRequest v2ProjectsRequest = new V2ProjectsRequest.Builder()
    .createdAt(DateTimeHelper.fromRfc8601DateTime("2018-09-27T20:10:35Z"))
    .description("My website API")
    .environment(Environment.PRODUCTION)
    .id(UUID.fromString("4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679"))
    .name("my-web-api")
    .ownerId(258992)
    .ownerUuid("99525febec065ca37b2ffe4f852fd2b2581895e7")
    .purpose("Service or API")
    .updatedAt(DateTimeHelper.fromRfc8601DateTime("2018-09-27T20:10:35Z"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



