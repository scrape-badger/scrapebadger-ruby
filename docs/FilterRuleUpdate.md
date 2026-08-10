# ScrapeBadger::FilterRuleUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tag** | **String** |  | [optional] |
| **query** | **String** |  | [optional] |
| **interval_seconds** | **Float** |  | [optional] |
| **max_results_per_poll** | **Integer** |  | [optional] |
| **status** | **String** |  | [optional] |
| **webhook_url** | **String** |  | [optional] |
| **webhook_secret** | **String** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::FilterRuleUpdate.new(
  tag: null,
  query: null,
  interval_seconds: null,
  max_results_per_poll: null,
  status: null,
  webhook_url: null,
  webhook_secret: null
)
```

