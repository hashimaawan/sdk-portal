# Reason

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/java/x-redirect/JTI0bSUyRlJlYXNvbg

The reason for the restriction. Albums may be restricted if the content is not available in a given market, to the user's subscription type, or when the user's account is set to not play explicit content.
Additional reasons may be added in the future.


# Enum Type Name

`Reason`


# Fields

| Name |
|  --- |
| `MARKET` |
| `PRODUCT` |
| `EXPLICIT` |


# Example

```java
import com.spotify.api.models.Reason;

Reason reason = Reason.PRODUCT;
```



