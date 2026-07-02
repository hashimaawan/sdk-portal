# V2 1 Clicks 401 Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjAxJTI1MjBDbGlja3MlMjUyMDQwMSUyNTIwRXJyb3I

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V21Clicks401ErrorException`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `string` | Required | A short identifier corresponding to the HTTP status code returned. For  example, the ID for a response returning a 404 status code would be "not_found." | getId(): string | setId(string id): void |
| `message` | `string` | Required | A message providing additional information about the error, including  details to help resolve it when possible. | getMessage(): string | setMessage(string message): void |
| `requestId` | `?string` | Optional | Optionally, some endpoints may include a request ID that should be  provided when reporting bugs or opening support tickets to help  identify the issue. | getRequestId(): ?string | setRequestId(?string requestId): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |



