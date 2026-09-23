# ScrapeBadger::VintedPhoto

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **url** | **String** |  |  |
| **dominant_color** | **String** |  | [optional] |
| **is_main** | **Boolean** |  | [optional][default to false] |
| **width** | **Integer** |  | [optional] |
| **height** | **Integer** |  | [optional] |
| **full_size_url** | **String** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::VintedPhoto.new(
  id: null,
  url: null,
  dominant_color: null,
  is_main: null,
  width: null,
  height: null,
  full_size_url: null
)
```

