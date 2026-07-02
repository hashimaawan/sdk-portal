# Droplet 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkRyb3BsZXQx

An object containing information about a resource scheduled for deletion.

*This model accepts additional fields of type Object.*


# Class Name

`Droplet1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DestroyedAt` | `LocalDateTime` | Optional | A time value given in ISO8601 combined date and time format indicating when the resource was destroyed if the request was successful. | LocalDateTime getDestroyedAt() | setDestroyedAt(LocalDateTime destroyedAt) |
| `ErrorMessage` | `String` | Optional | A string indicating that the resource was not successfully destroyed and providing additional information. | String getErrorMessage() | setErrorMessage(String errorMessage) |
| `Id` | `String` | Optional | The unique identifier for the resource scheduled for deletion. | String getId() | setId(String id) |
| `Name` | `String` | Optional | The name of the resource scheduled for deletion. | String getName() | setName(String name) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Droplet1;
import java.io.IOException;

Droplet1 droplet1 = new Droplet1.Builder()
    .destroyedAt(DateTimeHelper.fromRfc8601DateTime("2020-04-01T18:11:49Z"))
    .errorMessage("error_message0")
    .id("61486916")
    .name("ubuntu-s-1vcpu-1gb-nyc1-01-1585758823330")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



