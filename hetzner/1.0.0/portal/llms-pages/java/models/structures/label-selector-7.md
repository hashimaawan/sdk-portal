# Label Selector 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I3

Label selector and a list of selected targets


# Class Name

`LabelSelector7`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Selector` | `String` | Required | Label selector | String getSelector() | setSelector(String selector) |


# Example

```java
import cloud.hetzner.api.models.LabelSelector7;

LabelSelector7 labelSelector7 = new LabelSelector7.Builder(
    "env=prod"
)
.build();
```



