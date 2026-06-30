# Server 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlNlcnZlcjI

Configuration for type Server, required if type is `server`


# Class Name

`Server2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `int` | Required | ID of the Server | int getId() | setId(int id) |


# Example

```java
import cloud.hetzner.api.models.Server2;

Server2 server2 = new Server2.Builder(
    162
)
.build();
```



