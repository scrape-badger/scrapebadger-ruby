# ScrapeBadger::StreamMonitorCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **usernames** | **Array&lt;String&gt;** |  |  |
| **webhook_url** | **String** |  | [optional] |
| **webhook_secret** | **String** |  | [optional] |
| **filter_types** | **Array&lt;String&gt;** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::StreamMonitorCreate.new(
  name: null,
  usernames: null,
  webhook_url: null,
  webhook_secret: null,
  filter_types: null
)
```

