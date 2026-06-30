# Vault

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0bSUyRlZhdWx0

*This model accepts additional fields of type Object.*


# Class Name

`Vault`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AttributeVersion` | `Integer` | Optional | The vault version | Integer getAttributeVersion() | setAttributeVersion(Integer attributeVersion) |
| `ContentVersion` | `Integer` | Optional | The version of the vault contents | Integer getContentVersion() | setContentVersion(Integer contentVersion) |
| `CreatedAt` | `LocalDateTime` | Optional, Read-only | - | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `Description` | `String` | Optional | - | String getDescription() | setDescription(String description) |
| `Id` | `String` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` | String getId() | setId(String id) |
| `Items` | `Integer` | Optional | Number of active items in the vault | Integer getItems() | setItems(Integer items) |
| `Name` | `String` | Optional | - | String getName() | setName(String name) |
| `Type` | [`Type2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/enumerations/type-2.md) | Optional | - | Type2 getType() | setType(Type2 type) |
| `UpdatedAt` | `LocalDateTime` | Optional, Read-only | - | LocalDateTime getUpdatedAt() | setUpdatedAt(LocalDateTime updatedAt) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import java.io.IOException;
import local.m1password.ApiHelper;
import local.m1password.DateTimeHelper;
import local.m1password.models.Vault;

Vault vault = new Vault.Builder()
    .attributeVersion(108)
    .contentVersion(228)
    .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .description("description6")
    .id("id6")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



