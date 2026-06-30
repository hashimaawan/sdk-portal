# Error Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0bSUyRkVycm9yUmVzcG9uc2U

*This model accepts additional fields of type array.*


# Class Name

`ErrorResponseException`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `message` | `?string` | Optional | A message detailing the error | getMessage(): ?string | setMessage(?string message): void |
| `status` | `?int` | Optional | HTTP Status Code | getStatus(): ?int | setStatus(?int status): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |



