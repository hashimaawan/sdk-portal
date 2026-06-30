# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/ruby/x-redirect/JTI0bSUyRkltYWdl


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


# Example

```ruby
image = Image.new(
  '15',
  '200',
  'https://media1.giphy.com/media/cZ7rmKfFYOvYI/giphy.mp4',
  '25123',
  '32381',
  'https://media1.giphy.com/media/cZ7rmKfFYOvYI/200.gif',
  'https://media1.giphy.com/media/cZ7rmKfFYOvYI/giphy.webp',
  '12321',
  '320'
)
```



