# User Billing Address

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlVzZXJCaWxsaW5nQWRkcmVzcw

*This model accepts additional fields of type Object.*


# Class Name

`UserBillingAddress`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AddressLine1` | `String` | Optional | Street address line 1 | String getAddressLine1() | setAddressLine1(String addressLine1) |
| `AddressLine2` | `String` | Optional | Street address line 2 | String getAddressLine2() | setAddressLine2(String addressLine2) |
| `City` | `String` | Optional | City | String getCity() | setCity(String city) |
| `CountryIso2Code` | `String` | Optional | Country (ISO2) code | String getCountryIso2Code() | setCountryIso2Code(String countryIso2Code) |
| `CreatedAt` | `String` | Optional | Timestamp billing address was created | String getCreatedAt() | setCreatedAt(String createdAt) |
| `PostalCode` | `String` | Optional | Postal code | String getPostalCode() | setPostalCode(String postalCode) |
| `Region` | `String` | Optional | Region | String getRegion() | setRegion(String region) |
| `UpdatedAt` | `String` | Optional | Timestamp billing address was updated | String getUpdatedAt() | setUpdatedAt(String updatedAt) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.UserBillingAddress;
import java.io.IOException;

UserBillingAddress userBillingAddress = new UserBillingAddress.Builder()
    .addressLine1("101 Shark Row")
    .addressLine2("address_line24")
    .city("Atlantis")
    .countryIso2Code("US")
    .createdAt("2019-09-03T16:34:46.000+00:00")
    .postalCode("12345")
    .region("OC")
    .updatedAt("2019-09-03T16:34:46.000+00:00")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



