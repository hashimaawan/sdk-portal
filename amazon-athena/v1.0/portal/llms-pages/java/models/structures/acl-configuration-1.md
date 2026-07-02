# Acl Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkFjbENvbmZpZ3VyYXRpb24x

*This model accepts additional fields of type Object.*


# Class Name

`AclConfiguration1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `S3AclOption` | [`S3AclOption1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/s3-acl-option-1.md) | Required | - | S3AclOption1 getS3AclOption() | setS3AclOption(S3AclOption1 s3AclOption) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.AclConfiguration1;
import com.amazonaws.useast1.athena.models.S3AclOption1;
import java.io.IOException;

AclConfiguration1 aclConfiguration1 = new AclConfiguration1.Builder(
    S3AclOption1.BUCKET_OWNER_FULL_CONTROL
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



