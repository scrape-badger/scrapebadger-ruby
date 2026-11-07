# ScrapeBadger::GitHubProfileResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile** | [**GitHubProfile**](GitHubProfile.md) |  |  |
| **pinned_repositories** | [**Array&lt;GitHubRepository&gt;**](GitHubRepository.md) |  | [optional] |
| **popular_repositories** | [**Array&lt;GitHubRepository&gt;**](GitHubRepository.md) |  | [optional] |
| **readme** | [**GitHubReadme**](GitHubReadme.md) |  | [optional] |
| **organizations** | [**Array&lt;GitHubAccountPreview&gt;**](GitHubAccountPreview.md) |  | [optional] |
| **sponsors** | [**Array&lt;GitHubAccountPreview&gt;**](GitHubAccountPreview.md) |  | [optional] |
| **sponsoring** | [**Array&lt;GitHubAccountPreview&gt;**](GitHubAccountPreview.md) |  | [optional] |
| **additional_sponsors_count** | **Integer** |  | [optional] |
| **additional_sponsoring_count** | **Integer** |  | [optional] |
| **achievements** | [**Array&lt;GitHubAchievement&gt;**](GitHubAchievement.md) |  | [optional] |
| **highlights** | [**Array&lt;GitHubTextLink&gt;**](GitHubTextLink.md) |  | [optional] |
| **contributions** | [**GitHubContributions**](GitHubContributions.md) |  | [optional] |
| **repositories** | [**Array&lt;GitHubRepository&gt;**](GitHubRepository.md) |  | [optional] |
| **starred_repositories** | [**Array&lt;GitHubRepository&gt;**](GitHubRepository.md) |  | [optional] |
| **star_lists** | [**Array&lt;GitHubNamedLink&gt;**](GitHubNamedLink.md) |  | [optional] |
| **pagination** | [**GitHubPagination**](GitHubPagination.md) |  | [optional] |
| **top_languages** | [**Array&lt;GitHubLanguage&gt;**](GitHubLanguage.md) |  | [optional] |
| **topics** | **Array&lt;String&gt;** |  | [optional] |
| **people** | [**Array&lt;GitHubAccountPreview&gt;**](GitHubAccountPreview.md) |  | [optional] |
| **verified_domains** | **Array&lt;String&gt;** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::GitHubProfileResponse.new(
  profile: null,
  pinned_repositories: null,
  popular_repositories: null,
  readme: null,
  organizations: null,
  sponsors: null,
  sponsoring: null,
  additional_sponsors_count: null,
  additional_sponsoring_count: null,
  achievements: null,
  highlights: null,
  contributions: null,
  repositories: null,
  starred_repositories: null,
  star_lists: null,
  pagination: null,
  top_languages: null,
  topics: null,
  people: null,
  verified_domains: null
)
```

