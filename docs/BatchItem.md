# ScrapeBadger::BatchItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **method** | **String** |  | [optional][default to &#39;GET&#39;] |
| **path** | **String** |  |  |
| **query** | [**Hash&lt;String, BatchItemQueryValue&gt;**](BatchItemQueryValue.md) |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::BatchItem.new(
  method: null,
  path: null,
  query: null
)
```

