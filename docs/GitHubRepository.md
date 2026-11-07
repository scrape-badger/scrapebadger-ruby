# ScrapeBadger::GitHubRepository

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **position** | **Integer** |  |  |
| **name** | **String** |  |  |
| **full_name** | **String** |  |  |
| **owner** | [**GitHubAccountPreview**](GitHubAccountPreview.md) |  |  |
| **link** | **String** |  |  |
| **id** | **Integer** |  | [optional] |
| **description** | **String** |  | [optional] |
| **language** | **String** |  | [optional] |
| **language_color** | **String** |  | [optional] |
| **stars** | **Integer** |  | [optional] |
| **forks** | **Integer** |  | [optional] |
| **issues** | **Integer** |  | [optional] |
| **pull_requests** | **Integer** |  | [optional] |
| **stars_approximate** | **Boolean** |  | [optional] |
| **forks_approximate** | **Boolean** |  | [optional] |
| **issues_approximate** | **Boolean** |  | [optional] |
| **pull_requests_approximate** | **Boolean** |  | [optional] |
| **visibility** | **String** |  | [optional] |
| **is_fork** | **Boolean** |  | [optional] |
| **license** | **String** |  | [optional] |
| **topics** | **Array&lt;String&gt;** |  | [optional] |
| **participation** | **Array&lt;Integer&gt;** |  | [optional] |
| **updated_at** | **String** |  | [optional] |
| **updated_utc** | **Float** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::GitHubRepository.new(
  position: null,
  name: null,
  full_name: null,
  owner: null,
  link: null,
  id: null,
  description: null,
  language: null,
  language_color: null,
  stars: null,
  forks: null,
  issues: null,
  pull_requests: null,
  stars_approximate: null,
  forks_approximate: null,
  issues_approximate: null,
  pull_requests_approximate: null,
  visibility: null,
  is_fork: null,
  license: null,
  topics: null,
  participation: null,
  updated_at: null,
  updated_utc: null
)
```

