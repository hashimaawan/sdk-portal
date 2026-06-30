# Label Selector

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I


# Class Name

`LabelSelector`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Selector` | `String` | Required | Label selector | String getSelector() | setSelector(String selector) |


# Example

```java
import cloud.hetzner.api.models.LabelSelector;

LabelSelector labelSelector = new LabelSelector.Builder(
    "env=prod"
)
.build();
```



