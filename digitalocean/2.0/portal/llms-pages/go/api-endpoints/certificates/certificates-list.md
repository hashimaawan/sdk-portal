# Certificates List

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkNlcnRpZmljYXRlcyUyRmNlcnRpZmljYXRlc19saXN0

To list all of the certificates available on your account, send a GET request to `/v2/certificates`.

```go
CertificatesList(
    ctx context.Context,
    perPage *int,
    page *int) (
    models.ApiResponse[models.V2CertificatesResponse],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `perPage` | `*int` | Query, Optional | Number of items returned per page<br><br>**Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 200` |
| `page` | `*int` | Query, Optional | Which 'page' of paginated results to return.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |


# Response Type

**200**: The result will be a JSON object with a `certificates` key. This will be set to an array of certificate objects, each of which will contain the standard certificate attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2CertificatesResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-certificates-response.md).


# Example Usage

```go
ctx := context.Background()

perPage := 2

page := 1

apiResponse, err := certificatesApi.CertificatesList(ctx, &perPage, &page)
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


# Example Response *(as JSON)*

```json
{
  "certificates": [
    {
      "created_at": "2017-02-08T16:02:37Z",
      "dns_names": [
        ""
      ],
      "id": "892071a0-bb95-49bc-8021-3afd67a210bf",
      "name": "web-cert-01",
      "not_after": "2017-02-22T00:23:00Z",
      "sha1_fingerprint": "dfcc9f57d86bf58e321c2c6c31c7a971be244ac7",
      "state": "verified",
      "type": "custom"
    },
    {
      "created_at": "2018-03-09T18:44:11Z",
      "dns_names": [
        "www.example.com",
        "example.com"
      ],
      "id": "ba9b9c18-6c59-46c2-99df-70da170a42ba",
      "name": "web-cert-02",
      "not_after": "2018-06-07T17:44:12Z",
      "sha1_fingerprint": "479c82b5c63cb6d3e6fac4624d58a33b267e166c",
      "state": "verified",
      "type": "lets_encrypt"
    }
  ],
  "links": {},
  "meta": {
    "total": 2
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |



