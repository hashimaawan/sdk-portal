# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/ruby/x-redirect/JTI0bSUyRkltYWdl

*This model accepts additional fields of type Object.*


# Class Name

`Image`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `frames` | `String` | Optional | The number of frames in this GIF. |
| `height` | `String` | Optional | The height of this GIF in pixels. |
| `mp_4` | `String` | Optional | The URL for this GIF in .MP4 format. |
| `mp_4_size` | `String` | Optional | The size in bytes of the .MP4 file corresponding to this GIF. |
| `size` | `String` | Optional | The size of this GIF in bytes. |
| `url` | `String` | Optional | The publicly-accessible direct URL for this GIF. |
| `webp` | `String` | Optional | The URL for this GIF in .webp format. |
| `webp_size` | `String` | Optional | The size in bytes of the .webp file corresponding to this GIF. |
| `width` | `String` | Optional | The width of this GIF in pixels. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
image = Image.new(
  frames: '15',
  height: '200',
  mp4: 'https://media1.giphy.com/media/cZ7rmKfFYOvYI/giphy.mp4',
  mp4_size: '25123',
  size: '32381',
  url: 'https://media1.giphy.com/media/cZ7rmKfFYOvYI/200.gif',
  webp: 'https://media1.giphy.com/media/cZ7rmKfFYOvYI/giphy.webp',
  webp_size: '12321',
  width: '320',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



