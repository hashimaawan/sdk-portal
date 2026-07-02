# Invoice Preview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkludm9pY2VQcmV2aWV3

The invoice preview.

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`InvoicePreview`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount` | `str` | Optional | Total amount of the invoice, in USD.  This will reflect month-to-date usage in the invoice preview. |
| `invoice_period` | `str` | Optional | Billing period of usage for which the invoice is issued, in `YYYY-MM`  format. |
| `invoice_uuid` | `str` | Optional | The UUID of the invoice. The canonical reference for the invoice. |
| `updated_at` | `str` | Optional | Time the invoice was last updated.  This is only included with the invoice preview. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.invoice_preview import InvoicePreview

invoice_preview = InvoicePreview(
    amount='23.45',
    invoice_period='2020-01',
    invoice_uuid='fdabb512-6faf-443c-ba2e-665452332a9e',
    updated_at='2020-01-23T06:31:50Z',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



