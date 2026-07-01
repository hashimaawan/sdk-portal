# Images

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/typescript/x-redirect/JTI0bSUyRkltYWdlcw

An object containing data for various available formats and sizes of this GIF.

*This model accepts additional fields of type unknown.*


# Interface Name

`Images`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `downsized` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `downsizedLarge` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `downsizedMedium` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `downsizedSmall` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `downsizedStill` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `fixedHeight` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `fixedHeightDownsampled` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `fixedHeightSmall` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `fixedHeightSmallStill` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `fixedHeightStill` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `fixedWidth` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `fixedWidthDownsampled` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `fixedWidthSmall` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `fixedWidthSmallStill` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `fixedWidthStill` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `looping` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `original` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `originalStill` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `preview` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `previewGif` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Images } from 'giphy-apilib';

const images: Images = {
  downsized: {
    frames: 'frames0',
    height: 'height8',
    mp4: 'mp40',
    mp4Size: 'mp4_size2',
    size: 'size2',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  downsizedLarge: {
    frames: 'frames6',
    height: 'height4',
    mp4: 'mp46',
    mp4Size: 'mp4_size8',
    size: 'size8',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  downsizedMedium: {
    frames: 'frames2',
    height: 'height0',
    mp4: 'mp42',
    mp4Size: 'mp4_size4',
    size: 'size4',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  downsizedSmall: {
    frames: 'frames0',
    height: 'height8',
    mp4: 'mp40',
    mp4Size: 'mp4_size2',
    size: 'size2',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  downsizedStill: {
    frames: 'frames4',
    height: 'height4',
    mp4: 'mp46',
    mp4Size: 'mp4_size8',
    size: 'size2',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



