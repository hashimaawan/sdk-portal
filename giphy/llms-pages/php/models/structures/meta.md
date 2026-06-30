# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/php/x-redirect/JTI0bSUyRk1ldGE

The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances.


# Class Name

`Meta`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `msg` | `?string` | Optional | HTTP Response Message | getMsg(): ?string | setMsg(?string msg): void |
| `responseId` | `?string` | Optional | A unique ID paired with this response from the API. | getResponseId(): ?string | setResponseId(?string responseId): void |
| `status` | `?int` | Optional | HTTP Response Code | getStatus(): ?int | setStatus(?int status): void |


# Example

```php
use GiphyAPILib\Models\Builders\MetaBuilder;

$meta = MetaBuilder::init()
    ->msg('OK')
    ->responseId('57eea03c72381f86e05c35d2')
    ->status(200)
    ->build();
```



