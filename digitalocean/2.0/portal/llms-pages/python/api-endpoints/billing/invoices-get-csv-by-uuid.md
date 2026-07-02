# Invoices Get Csv by UUID

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0ZSUyRkJpbGxpbmclMkZpbnZvaWNlc19nZXRfY3N2QnlVVUlE

To retrieve a CSV for an invoice, send a GET request to `/v2/customers/my/invoices/$INVOICE_UUID/csv`.

```python
def invoices_get_csv_by_uuid(self,
                            invoice_uuid)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `invoice_uuid` | `str` | Template, Required | UUID of the invoice |


# Response Type

**200**: The response will be a CSV file.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type `str`.


# Example Usage

```python
invoice_uuid = '22737513-0ea7-4206-8ceb-98a575af7681'

result = billing_api.invoices_get_csv_by_uuid(invoice_uuid)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Example Response

```
"product,group_description,description,hours,start,end,USD,project_name,category\nFloating IPs,,Unused Floating IP - 1.1.1.1,100,2020-07-01 00:00:00 +0000,2020-07-22 18:14:39 +0000,$3.11,,iaas\nTaxes,,STATE SALES TAX (6.25%),,2020-07-01 00:00:00 +0000,2020-07-31 23:59:59 +0000,$0.16,,iaas\n"
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |



