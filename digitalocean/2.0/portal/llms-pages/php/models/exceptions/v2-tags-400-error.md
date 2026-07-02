# V2 Tags 400 Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBUYWdzJTI1MjA0MDAlMjUyMEVycm9y

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2Tags400ErrorException`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `error` | `string` | Required | A message providing information about the error. | getError(): string | setError(string error): void |
| `messages` | `?(string[])` | Optional | A list of error messages. | getMessages(): ?array | setMessages(?array messages): void |
| `rootCauses` | `string[]` | Required | A list of underlying causes for the error, including details to help  resolve it when possible. | getRootCauses(): array | setRootCauses(array rootCauses): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |



