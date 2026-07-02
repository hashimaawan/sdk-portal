# V2 Tags 400 Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBUYWdzJTI1MjA0MDAlMjUyMEVycm9y

*This model accepts additional fields of type Object.*


# Class Name

`V2Tags400ErrorException`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Error` | `String` | Required | A message providing information about the error. | String getError() | setError(String error) |
| `Messages` | `List<String>` | Optional | A list of error messages. | List<String> getMessages() | setMessages(List<String> messages) |
| `RootCauses` | `List<String>` | Required | A list of underlying causes for the error, including details to help  resolve it when possible. | List<String> getRootCauses() | setRootCauses(List<String> rootCauses) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
try {
    // make the API call
} catch (V2Tags400ErrorException e) {
    e.printStackTrace();
} catch (ApiException e) {
    e.printStackTrace();
}
```



