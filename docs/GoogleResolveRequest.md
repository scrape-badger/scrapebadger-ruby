# ScrapeBadger::GoogleResolveRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **results** | [**Array&lt;GoogleResolveItem&gt;**](GoogleResolveItem.md) | The results to resolve, 1 to 25. Each needs a &#x60;link_token&#x60;. Any other field (&#x60;position&#x60;, &#x60;title&#x60;, your own id) is returned unchanged on its row, so the &#x60;organic_results&#x60; items of a search response can be sent as they are. |  |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::GoogleResolveRequest.new(
  results: null
)
```

