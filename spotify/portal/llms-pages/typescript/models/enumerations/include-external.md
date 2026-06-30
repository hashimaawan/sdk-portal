# Include External

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRkluY2x1ZGUlMjUyMEV4dGVybmFs

If `include_external=audio` is specified it signals that the client can play externally hosted audio content, and marks
the content as playable in the response. By default externally hosted audio content is marked as unplayable in the response.


# Enum Type Name

`IncludeExternal`


# Fields

| Name |
|  --- |
| `Audio` |


# Example

```ts
import {
  IncludeExternal,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const includeExternal = IncludeExternal.Audio;
```



