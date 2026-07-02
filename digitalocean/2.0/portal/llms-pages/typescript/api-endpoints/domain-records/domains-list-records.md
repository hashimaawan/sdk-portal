# Domains List Records

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRkRvbWFpbiUyNTIwUmVjb3JkcyUyRmRvbWFpbnNfbGlzdF9yZWNvcmRz

To get a listing of all records configured for a domain, send a GET request to `/v2/domains/$DOMAIN_NAME/records`.
The list of records returned can be filtered by using the `name` and `type` query parameters. For example, to only include A records for a domain, send a GET request to `/v2/domains/$DOMAIN_NAME/records?type=A`. `name` must be a fully qualified record name. For example, to only include records matching `sub.example.com`, send a GET request to `/v2/domains/$DOMAIN_NAME/records?name=sub.example.com`. Both name and type may be used together.

```ts
async domainsListRecords(
  domainName: string,
  name?: string,
  type?: Type8,
  perPage?: number,
  page?: number,
  requestOptions?: RequestOptions
): Promise<ApiResponse<V2DomainsRecordsResponse>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `domainName` | `string` | Template, Required | The name of the domain itself. |
| `name` | `string \| undefined` | Query, Optional | A fully qualified record name. For example, to only include records matching sub.example.com, send a GET request to `/v2/domains/$DOMAIN_NAME/records?name=sub.example.com`. |
| `type` | [`Type8 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/type-8.md) | Query, Optional | The type of the DNS record. For example: A, CNAME, TXT, ... |
| `perPage` | `number \| undefined` | Query, Optional | Number of items returned per page<br><br>**Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 200` |
| `page` | `number \| undefined` | Query, Optional | Which 'page' of paginated results to return.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: The response will be a JSON object with a key called `domain_records`. The value of this will be an array of domain record objects, each of which contains the standard domain record attributes. For attributes that are not used by a specific record type, a value of `null` will be returned. For instance, all records other than SRV will have `null` for the `weight` and `port` attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2DomainsRecordsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-domains-records-response.md).


# Example Usage

```ts
const domainName = 'example.com';

const name = 'sub.example.com';

const type = Type8.A;

const perPage = 2;

const page = 1;

try {
  const response = await domainRecordsApi.domainsListRecords(
    domainName,
    name,
    type,
    perPage,
    page
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
    if (error instanceof V21Clicks401Error) {
      console.log(error.result);
    }
  }
}
```


# Example Response *(as JSON)*

```json
{
  "domain_records": [
    {
      "data": "ns1.digitalocean.com",
      "flags": null,
      "id": 28448429,
      "name": "@",
      "port": null,
      "priority": null,
      "tag": null,
      "ttl": 1800,
      "type": "NS",
      "weight": null
    },
    {
      "data": "ns2.digitalocean.com",
      "flags": null,
      "id": 28448430,
      "name": "@",
      "port": null,
      "priority": null,
      "tag": null,
      "ttl": 1800,
      "type": "NS",
      "weight": null
    },
    {
      "data": "ns3.digitalocean.com",
      "flags": null,
      "id": 28448431,
      "name": "@",
      "port": null,
      "priority": null,
      "tag": null,
      "ttl": 1800,
      "type": "NS",
      "weight": null
    },
    {
      "data": "1.2.3.4",
      "flags": null,
      "id": 28448432,
      "name": "@",
      "port": null,
      "priority": null,
      "tag": null,
      "ttl": 1800,
      "type": "A",
      "weight": null
    }
  ],
  "links": {},
  "meta": {
    "total": 4
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |



