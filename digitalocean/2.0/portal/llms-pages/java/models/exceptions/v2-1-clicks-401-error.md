# V2 1 Clicks 401 Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjAxJTI1MjBDbGlja3MlMjUyMDQwMSUyNTIwRXJyb3I

*This model accepts additional fields of type Object.*


# Class Name

`V21Clicks401ErrorException`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | A short identifier corresponding to the HTTP status code returned. For  example, the ID for a response returning a 404 status code would be "not_found." | String getId() | setId(String id) |
| `Message` | `String` | Required | A message providing additional information about the error, including  details to help resolve it when possible. | String getMessageField() | setMessageField(String messageField) |
| `RequestId` | `String` | Optional | Optionally, some endpoints may include a request ID that should be  provided when reporting bugs or opening support tickets to help  identify the issue. | String getRequestId() | setRequestId(String requestId) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
try {
    // make the API call
} catch (V21Clicks401ErrorException e) {
    e.printStackTrace();
} catch (ApiException e) {
    e.printStackTrace();
}
```



