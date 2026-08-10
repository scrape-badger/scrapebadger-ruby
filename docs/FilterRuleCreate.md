# ScrapeBadger::FilterRuleCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tag** | **String** |  |  |
| **query** | **String** |  |  |
| **interval_seconds** | **Float** |  |  |
| **max_results_per_poll** | **Integer** |  | [optional][default to 20] |
| **webhook_url** | **String** |  | [optional] |
| **webhook_secret** | **String** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::FilterRuleCreate.new(
  tag: null,
  query: null,
  interval_seconds: null,
  max_results_per_poll: null,
  webhook_url: null,
  webhook_secret: null
)
```

