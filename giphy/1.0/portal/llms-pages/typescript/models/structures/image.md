# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/typescript/x-redirect/JTI0bSUyRkltYWdl

*This model accepts additional fields of type unknown.*


# Interface Name

`Image`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `frames` | `string \| undefined` | Optional | The number of frames in this GIF. |
| `height` | `string \| undefined` | Optional | The height of this GIF in pixels. |
| `mp4` | `string \| undefined` | Optional | The URL for this GIF in .MP4 format. |
| `mp4Size` | `string \| undefined` | Optional | The size in bytes of the .MP4 file corresponding to this GIF. |
| `size` | `string \| undefined` | Optional | The size of this GIF in bytes. |
| `url` | `string \| undefined` | Optional | The publicly-accessible direct URL for this GIF. |
| `webp` | `string \| undefined` | Optional | The URL for this GIF in .webp format. |
| `webpSize` | `string \| undefined` | Optional | The size in bytes of the .webp file corresponding to this GIF. |
| `width` | `string \| undefined` | Optional | The width of this GIF in pixels. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Image } from 'giphy-apilib';

const image: Image = {
  frames: '15',
  height: '200',
  mp4: 'https://media1.giphy.com/media/cZ7rmKfFYOvYI/giphy.mp4',
  mp4Size: '25123',
  size: '32381',
  url: 'https://media1.giphy.com/media/cZ7rmKfFYOvYI/200.gif',
  webp: 'https://media1.giphy.com/media/cZ7rmKfFYOvYI/giphy.webp',
  webpSize: '12321',
  width: '320',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



