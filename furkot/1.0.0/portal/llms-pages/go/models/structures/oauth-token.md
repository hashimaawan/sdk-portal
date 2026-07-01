# OAuth Token

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/go/x-redirect/JTI0bSUyRk9BdXRoVG9rZW4

OAuth 2 Authorization endpoint response


# Class Name

`OauthToken`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AccessToken` | `string` | Required | Access token |
| `TokenType` | `string` | Required | Type of access token |
| `ExpiresIn` | `*int64` | Optional | Time in seconds before the access token expires |
| `Scope` | `*string` | Optional | List of scopes granted<br>This is a space-delimited list of strings. |
| `Expiry` | `*int64` | Optional | Time of token expiry as unix timestamp (UTC) |
| `RefreshToken` | `*string` | Optional | Refresh token<br>Used to get a new access token when it expires. |


# Example

```go
package main

import (
    "furkotTrips/models"
)

func main() {
    oauthToken := models.OauthToken{
        AccessToken:  "access_token8",
        TokenType:    "token_type8",
        ExpiresIn:    models.ToPointer(int64(10)),
        Scope:        models.ToPointer("scope2"),
        Expiry:       models.ToPointer(int64(152)),
        RefreshToken: models.ToPointer("refresh_token0"),
    }

}
```



