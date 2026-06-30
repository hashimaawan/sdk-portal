# Forbidden

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/java/x-redirect/JTI0bSUyRkZvcmJpZGRlbg

*This model accepts additional fields of type Object.*


# Class Name

`ForbiddenException`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Error` | [`ErrorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/java/models/structures/error-object.md) | Required | - | ErrorObject getError() | setError(ErrorObject error) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
try {
    // make the API call
} catch (ForbiddenException e) {
    e.printStackTrace();
} catch (ApiException e) {
    e.printStackTrace();
}
```



