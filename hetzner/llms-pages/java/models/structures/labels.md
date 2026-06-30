# Labels

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkxhYmVscw

User-defined labels (key-value pairs)


# Class Name

`Labels`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Labelkey` | `String` | Optional | New label | String getLabelkey() | setLabelkey(String labelkey) |


# Example

```java
import cloud.hetzner.api.models.Labels;

Labels labels = new Labels.Builder()
    .labelkey("value")
    .build();
```



