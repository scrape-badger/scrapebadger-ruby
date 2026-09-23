# ScrapeBadger::VintedUserProfile

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **login** | **String** |  |  |
| **photo_url** | **String** |  | [optional] |
| **business** | **Boolean** |  | [optional][default to false] |
| **country_code** | **String** |  | [optional] |
| **city** | **String** |  | [optional] |
| **feedback_count** | **Integer** |  | [optional][default to 0] |
| **feedback_reputation** | **Float** |  | [optional][default to 0.0] |
| **positive_feedback_count** | **Integer** |  | [optional][default to 0] |
| **neutral_feedback_count** | **Integer** |  | [optional][default to 0] |
| **negative_feedback_count** | **Integer** |  | [optional][default to 0] |
| **item_count** | **Integer** |  | [optional][default to 0] |
| **total_items_count** | **Integer** |  | [optional][default to 0] |
| **followers_count** | **Integer** |  | [optional][default to 0] |
| **following_count** | **Integer** |  | [optional][default to 0] |
| **is_online** | **Boolean** |  | [optional][default to false] |
| **is_on_holiday** | **Boolean** |  | [optional][default to false] |
| **last_loged_on_ts** | **String** |  | [optional] |
| **profile_url** | **String** |  | [optional] |
| **locale** | **String** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::VintedUserProfile.new(
  id: null,
  login: null,
  photo_url: null,
  business: null,
  country_code: null,
  city: null,
  feedback_count: null,
  feedback_reputation: null,
  positive_feedback_count: null,
  neutral_feedback_count: null,
  negative_feedback_count: null,
  item_count: null,
  total_items_count: null,
  followers_count: null,
  following_count: null,
  is_online: null,
  is_on_holiday: null,
  last_loged_on_ts: null,
  profile_url: null,
  locale: null
)
```

