# Time Interval Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRlRpbWVJbnRlcnZhbE9iamVjdA

*This model accepts additional fields of type object.*


# Class Name

`TimeIntervalObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Start` | `double?` | Optional | The starting point (in seconds) of the time interval. |
| `Duration` | `double?` | Optional | The duration (in seconds) of the time interval. |
| `Confidence` | `double?` | Optional | The confidence, from 0.0 to 1.0, of the reliability of the interval.<br><br>**Constraints**: `>= 0`, `<= 1` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

TimeIntervalObject timeIntervalObject = new TimeIntervalObject
{
    Start = 0.49567,
    Duration = 2.18749,
    Confidence = 0.925,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



