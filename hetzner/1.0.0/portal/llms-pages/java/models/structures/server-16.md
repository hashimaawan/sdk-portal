# Server 16

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlcjE2

Configuration for type Server, required if type is `server`


# Class Name

`Server16`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `double` | Required | ID of the Server | double getId() | setId(double id) |


# Example

```java
import cloud.hetzner.api.models.Server16;

Server16 server16 = new Server16.Builder(
    80D
)
.build();
```



