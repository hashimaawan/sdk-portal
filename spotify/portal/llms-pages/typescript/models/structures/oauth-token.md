# OAuth Token

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRk9BdXRoVG9rZW4

OAuth 2 Authorization endpoint response


# Interface Name

`OauthToken`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accessToken` | `string` | Required | Access token |
| `tokenType` | `string` | Required | Type of access token |
| `expiresIn` | `bigint \| undefined` | Optional | Time in seconds before the access token expires |
| `scope` | `string \| undefined` | Optional | List of scopes granted<br>This is a space-delimited list of strings. |
| `expiry` | `bigint \| undefined` | Optional | Time of token expiry as unix timestamp (UTC) |
| `refreshToken` | `string \| undefined` | Optional | Refresh token<br>Used to get a new access token when it expires. |


# Example

```ts
import {
  OauthToken,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const oauthToken: OauthToken = {
  accessToken: 'access_token8',
  tokenType: 'token_type8',
  expiresIn: BigInt(10),
  scope: 'scope2',
  expiry: BigInt(152),
  refreshToken: 'refresh_token0',
};
```



