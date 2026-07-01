# Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkVycm9y

Error message for the Action if error occurred, otherwise null


# Class Name

`Error`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Code` | `String` | Required | Fixed machine readable code | String getCode() | setCode(String code) |
| `Message` | `String` | Required | Humanized error message | String getMessage() | setMessage(String message) |


# Example

```java
import cloud.hetzner.api.models.Error;

Error error = new Error.Builder(
    "action_failed",
    "Action failed"
)
.build();
```



