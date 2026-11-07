# ScrapeBadger::GitHubContributions

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **total** | **Integer** |  |  |
| **calendar** | [**Array&lt;GitHubCalendarDay&gt;**](GitHubCalendarDay.md) |  |  |
| **from** | **Date** |  |  |
| **to** | **Date** |  |  |
| **activity_overview** | [**GitHubActivityOverview**](GitHubActivityOverview.md) |  | [optional] |
| **activity** | [**Array&lt;GitHubActivityBlock&gt;**](GitHubActivityBlock.md) |  | [optional] |
| **private_contributions** | **Integer** |  | [optional] |
| **activity_from** | **String** |  | [optional] |
| **activity_to** | **String** |  | [optional] |
| **previous_activity_url** | **String** |  | [optional] |
| **years** | **Array&lt;Integer&gt;** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::GitHubContributions.new(
  total: null,
  calendar: null,
  from: null,
  to: null,
  activity_overview: null,
  activity: null,
  private_contributions: null,
  activity_from: null,
  activity_to: null,
  previous_activity_url: null,
  years: null
)
```

