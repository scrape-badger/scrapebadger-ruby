# ScrapeBadger::ExtractRequestExtractRulesValue

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **selector** | **String** | CSS or XPath selector. |  |
| **type** | **String** |  | [optional] |
| **all** | **Boolean** | Return every match as a list, not just the first. | [optional][default to false] |
| **output** | **String** | An element&#39;s text content, or its outer HTML. | [optional][default to &#39;text&#39;] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::ExtractRequestExtractRulesValue.new(
  selector: null,
  type: null,
  all: null,
  output: null
)
```

