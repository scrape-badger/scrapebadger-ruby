# ScrapeBadger::BatchRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **requests** | [**Array&lt;BatchItem&gt;**](BatchItem.md) |  |  |
| **callback_url** | **String** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::BatchRequest.new(
  requests: null,
  callback_url: null
)
```

