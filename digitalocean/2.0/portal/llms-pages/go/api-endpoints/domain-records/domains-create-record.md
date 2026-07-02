# Domains Create Record

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkRvbWFpbiUyNTIwUmVjb3JkcyUyRmRvbWFpbnNfY3JlYXRlX3JlY29yZA

To create a new record to a domain, send a POST request to
`/v2/domains/$DOMAIN_NAME/records`.

The request must include all of the required fields for the domain record type
being added.

See the [attribute table](#tag/Domain-Records) for details regarding record
types and their respective required attributes.

```go
DomainsCreateRecord(
    ctx context.Context,
    domainName string,
    body *models.DomainsCreateRecordBody) (
    models.ApiResponse[models.V2DomainsRecordsResponse1],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `domainName` | `string` | Template, Required | The name of the domain itself. |
| `body` | [`*models.DomainsCreateRecordBody`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/oneof-anyof-definitions/domains-create-record-body.md) | Body, Optional | This is a container for any-of cases. |


# Response Type

**201**: The response body will be a JSON object with a key called `domain_record`. The value of this will be an object representing the new record. Attributes that are not applicable for the record type will be set to `null`. An `id` attribute is generated for each record as part of the object.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2DomainsRecordsResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-domains-records-response-1.md).


# Example Usage

```go
ctx := context.Background()

domainName := "example.com"

body := models.DomainsCreateRecordBodyContainer.FromV2DomainsRecordsRequest(models.V2DomainsRecordsRequest{
    Data:                  "162.10.66.0",
    Flags:                 models.NewOptional[int](nil),
    Name:                  "www",
    Port:                  models.NewOptional[int](nil),
    Priority:              models.NewOptional[int](nil),
    Tag:                   models.NewOptional[string](nil),
    Ttl:                   models.ToPointer(1800),
    Type:                  "A",
    Weight:                models.NewOptional[int](nil),
})

apiResponse, err := domainRecordsApi.DomainsCreateRecord(ctx, domainName, &body)
if err != nil {
    switch typedErr := err.(type) {
        case *errors.V21Clicks401Error:
            log.Fatalln("V21Clicks401ErrorException: ", typedErr)
        default:
            log.Fatalln(err)
    }
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |



