# ScrapeBadger::StreamMonitorUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  | [optional] |
| **usernames** | **Array&lt;String&gt;** |  | [optional] |
| **status** | **String** |  | [optional] |
| **webhook_url** | **String** |  | [optional] |
| **webhook_secret** | **String** |  | [optional] |
| **filter_types** | **Array&lt;String&gt;** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::StreamMonitorUpdate.new(
  name: null,
  usernames: null,
  status: null,
  webhook_url: null,
  webhook_secret: null,
  filter_types: null
)
```

