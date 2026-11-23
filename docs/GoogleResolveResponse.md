# ScrapeBadger::GoogleResolveResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **results** | [**Array&lt;GoogleResolveRow&gt;**](GoogleResolveRow.md) | One row for each result sent, in the order sent. |  |
| **retry_after_seconds** | **Integer** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::GoogleResolveResponse.new(
  results: null,
  retry_after_seconds: null
)
```

