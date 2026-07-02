# Domains Patch Record

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkRvbWFpbiUyNTIwUmVjb3JkcyUyRmRvbWFpbnNfcGF0Y2hfcmVjb3Jk

To update an existing record, send a PATCH request to
`/v2/domains/$DOMAIN_NAME/records/$DOMAIN_RECORD_ID`. Any attribute valid for
the record type can be set to a new value for the record.

See the [attribute table](#tag/Domain-Records) for details regarding record
types and their respective attributes.

```go
DomainsPatchRecord(
    ctx context.Context,
    domainName string,
    domainRecordId int,
    body *models.DomainRecord) (
    models.ApiResponse[models.V2DomainsRecordsResponse1],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `domainName` | `string` | Template, Required | The name of the domain itself. |
| `domainRecordId` | `int` | Template, Required | The unique identifier of the domain record. |
| `body` | [`*models.DomainRecord`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/domain-record.md) | Body, Optional | - |


# Response Type

**200**: The response will be a JSON object with a key called `domain_record`. The value of this will be a domain record object which contains the standard domain record attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2DomainsRecordsResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-domains-records-response-1.md).


# Example Usage

```go
ctx := context.Background()

domainName := "example.com"

domainRecordId := 3352896

body := models.DomainRecord{
    Name:                  models.ToPointer("blog"),
    Type:                  "A",
}

apiResponse, err := domainRecordsApi.DomainsPatchRecord(ctx, domainName, domainRecordId, &body)
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



