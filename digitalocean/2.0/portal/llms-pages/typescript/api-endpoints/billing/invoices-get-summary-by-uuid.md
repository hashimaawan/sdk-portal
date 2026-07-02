# Invoices Get Summary by UUID

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRkJpbGxpbmclMkZpbnZvaWNlc19nZXRfc3VtbWFyeUJ5VVVJRA

To retrieve a summary for an invoice, send a GET request to `/v2/customers/my/invoices/$INVOICE_UUID/summary`.

```ts
async invoicesGetSummaryByUuid(
  invoiceUuid: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<V2CustomersMyInvoicesSummaryResponse>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `invoiceUuid` | `string` | Template, Required | UUID of the invoice |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: To retrieve a summary for an invoice, send a GET request to  `/v2/customers/my/invoices/$INVOICE_UUID/summary`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2CustomersMyInvoicesSummaryResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-customers-my-invoices-summary-response.md).


# Example Usage

```ts
const invoiceUuid = '22737513-0ea7-4206-8ceb-98a575af7681';

try {
  const response = await billingApi.invoicesGetSummaryByUuid(invoiceUuid);

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
  "amount": "27.13",
  "billing_period": "2020-01",
  "credits_and_adjustments": {
    "amount": "6.78",
    "name": "Credits & adjustments"
  },
  "invoice_uuid": "22737513-0ea7-4206-8ceb-98a575af7681",
  "overages": {
    "amount": "3.45",
    "name": "Overages"
  },
  "product_charges": {
    "amount": "12.34",
    "items": [
      {
        "amount": "10.00",
        "count": "1",
        "name": "Spaces Subscription"
      },
      {
        "amount": "2.34",
        "count": "1",
        "name": "Database Clusters"
      }
    ],
    "name": "Product usage charges"
  },
  "taxes": {
    "amount": "4.56",
    "name": "Taxes"
  },
  "user_billing_address": {
    "address_line1": "101 Shark Row",
    "city": "Atlantis",
    "country_iso2_code": "US",
    "created_at": "2019-09-03T16:34:46.000+00:00",
    "postal_code": "12345",
    "region": "OC",
    "updated_at": "2019-09-03T16:34:46.000+00:00"
  },
  "user_company": "DigitalOcean",
  "user_email": "sammy@digitalocean.com",
  "user_name": "Sammy Shark"
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



