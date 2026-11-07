# ScrapeBadger::YelpHours

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **day** | **String** |  |  |
| **open** | **String** | Local wall time HH:MM. |  |
| **close** | **String** | Local wall time HH:MM; may be past midnight. |  |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::YelpHours.new(
  day: null,
  open: null,
  close: null
)
```

