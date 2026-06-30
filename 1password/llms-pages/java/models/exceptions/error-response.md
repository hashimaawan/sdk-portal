# Error Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0bSUyRkVycm9yUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`ErrorResponseException`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Message` | `String` | Optional | A message detailing the error | String getMessageField() | setMessageField(String messageField) |
| `Status` | `Integer` | Optional | HTTP Status Code | Integer getStatus() | setStatus(Integer status) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
try {
    // make the API call
} catch (ErrorResponseException e) {
    e.printStackTrace();
} catch (ApiException e) {
    e.printStackTrace();
}
```



