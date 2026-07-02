# Apps List Regions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2xpc3RfcmVnaW9ucw

List all regions supported by App Platform.

```csharp
AppsListRegionsAsync()
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Response Type

**200**: A JSON object with key `regions`

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.V2AppsRegionsResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-apps-regions-response.md).


# Example Usage

```csharp
try
{
    ApiResponse<V2AppsRegionsResponse> result = await appsApi.AppsListRegionsAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
    if (e is V21Clicks401ErrorException)
    {
       // TODO: Handle V21Clicks401ErrorException exception here
    }
}
```


# Example Response *(as JSON)*

```json
{
  "regions": [
    {
      "continent": "Europe",
      "data_centers": [
        "ams3"
      ],
      "flag": "netherlands",
      "label": "Amsterdam",
      "slug": "ams"
    },
    {
      "continent": "North America",
      "data_centers": [
        "nyc1",
        "nyc3"
      ],
      "default": true,
      "flag": "usa",
      "label": "New York",
      "slug": "nyc"
    },
    {
      "continent": "Europe",
      "data_centers": [
        "fra1"
      ],
      "flag": "germany",
      "label": "Frankfurt",
      "slug": "fra"
    },
    {
      "continent": "North America",
      "data_centers": [
        "sfo3"
      ],
      "flag": "usa",
      "label": "San Francisco",
      "slug": "sfo"
    },
    {
      "continent": "Asia",
      "data_centers": [
        "sgp1"
      ],
      "flag": "singapore",
      "label": "Singapore",
      "slug": "sgp"
    },
    {
      "continent": "Asia",
      "data_centers": [
        "blr1"
      ],
      "flag": "india",
      "label": "Bangalore",
      "slug": "blr"
    },
    {
      "continent": "North America",
      "data_centers": [
        "tor1"
      ],
      "flag": "canada",
      "label": "Toronto",
      "slug": "tor"
    },
    {
      "continent": "Europe",
      "data_centers": [
        "lon1"
      ],
      "flag": "uk",
      "label": "London",
      "slug": "lon"
    }
  ]
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |



