# User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/typescript/x-redirect/JTI0bSUyRlVzZXI

The User Object contains information about the user associated with a GIF and URLs to assets such as that user's avatar image, profile, and more.


# Interface Name

`User`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `avatarUrl` | `string \| undefined` | Optional | The URL for this user's avatar image. |
| `bannerUrl` | `string \| undefined` | Optional | The URL for the banner image that appears atop this user's profile page. |
| `displayName` | `string \| undefined` | Optional | The display name associated with this user (contains formatting the base username might not). |
| `profileUrl` | `string \| undefined` | Optional | The URL for this user's profile. |
| `twitter` | `string \| undefined` | Optional | The Twitter username associated with this user, if applicable. |
| `username` | `string \| undefined` | Optional | The username associated with this user. |


# Example

```ts
import { User } from 'giphy-apilib';

const user: User = {
  avatarUrl: 'https://media1.giphy.com/avatars/election2016/XwYrZi5H87o6.gif',
  bannerUrl: 'https://media4.giphy.com/avatars/cheezburger/XkuejOhoGLE6.jpg',
  displayName: 'JoeCool4000',
  profileUrl: 'https://giphy.com/cheezburger/',
  twitter: '@joecool4000',
  username: 'joecool4000',
};
```



