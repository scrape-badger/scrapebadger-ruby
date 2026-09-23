# ScrapeBadger::VintedSellerSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **login** | **String** |  | [optional][default to &#39;&#39;] |
| **photo_url** | **String** |  | [optional] |
| **business** | **Boolean** |  | [optional][default to false] |
| **feedback_count** | **Integer** |  | [optional][default to 0] |
| **feedback_reputation** | **Float** |  | [optional][default to 0.0] |
| **item_count** | **Integer** |  | [optional][default to 0] |
| **location** | **String** |  | [optional] |
| **last_seen** | **String** |  | [optional] |
| **badges** | **Array&lt;String&gt;** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::VintedSellerSummary.new(
  id: null,
  login: null,
  photo_url: null,
  business: null,
  feedback_count: null,
  feedback_reputation: null,
  item_count: null,
  location: null,
  last_seen: null,
  badges: null
)
```

