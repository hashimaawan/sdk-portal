# Effect

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkVmZmVjdA

How the node reacts to pods that it won't tolerate. Available effect values are `NoSchedule`, `PreferNoSchedule`, and `NoExecute`.


# Enum Type Name

`Effect`


# Fields

| Name |
|  --- |
| `NOSCHEDULE` |
| `PREFERNOSCHEDULE` |
| `NOEXECUTE` |


# Example

```java
import com.digitalocean.api.models.Effect;

Effect effect = Effect.NOSCHEDULE;
```



