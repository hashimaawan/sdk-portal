# Trip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlRyaXA

*This model accepts additional fields of type object.*


# Class Name

`Trip`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Begin` | `DateTime?` | Optional | begin of the trip in its local timezone as YYYY-MM-DDThh:mm |
| `Description` | `string` | Optional | description of the trip (truncated to 200 characters) |
| `End` | `DateTime?` | Optional | end of the trip in its local timezone as YYYY-MM-DDThh:mm |
| `Id` | `string` | Optional | Unique ID of the trip |
| `Name` | `string` | Optional | name of the trip |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using FurkotTrips.Standard.Models;
using FurkotTrips.Standard.Utilities;
using System.Globalization;

Trip trip = new Trip
{
    Begin = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Description = "description8",
    End = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Id = "id8",
    Name = "name8",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



