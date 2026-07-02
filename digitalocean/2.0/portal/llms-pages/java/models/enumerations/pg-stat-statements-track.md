# Pg Stat Statements Track

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlBnU3RhdFN0YXRlbWVudHNUcmFjaw

Controls which statements are counted. Specify 'top' to track top-level statements (those issued directly by clients), 'all' to also track nested statements (such as statements invoked within functions), or 'none' to disable statement statistics collection. The default value is top.


# Enum Type Name

`PgStatStatementsTrack`


# Fields

| Name |
|  --- |
| `ALL` |
| `TOP` |
| `NONE` |


# Example

```java
import com.digitalocean.api.models.PgStatStatementsTrack;

PgStatStatementsTrack pgStatStatementsTrack = PgStatStatementsTrack.TOP;
```



