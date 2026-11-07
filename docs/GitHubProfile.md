# ScrapeBadger::GitHubProfile

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **login** | **String** |  |  |
| **link** | **String** |  |  |
| **is_organization** | **Boolean** |  |  |
| **id** | **Integer** |  | [optional] |
| **node_id** | **String** |  | [optional] |
| **type** | **String** |  | [optional] |
| **user_view_type** | **String** |  | [optional] |
| **site_admin** | **Boolean** |  | [optional] |
| **name** | **String** |  | [optional] |
| **avatar_url** | **String** |  | [optional] |
| **bio** | **String** |  | [optional] |
| **description** | **String** |  | [optional] |
| **pronouns** | **String** |  | [optional] |
| **local_time** | **String** |  | [optional] |
| **utc_offset** | **Float** |  | [optional] |
| **company** | **String** |  | [optional] |
| **location** | **String** |  | [optional] |
| **email** | **String** |  | [optional] |
| **website** | **String** |  | [optional] |
| **twitter_username** | **String** |  | [optional] |
| **hireable** | **Boolean** |  | [optional] |
| **social_accounts** | [**Array&lt;GitHubSocialAccount&gt;**](GitHubSocialAccount.md) |  | [optional] |
| **status** | [**GitHubStatus**](GitHubStatus.md) |  | [optional] |
| **followers** | **Integer** |  | [optional] |
| **following** | **Integer** |  | [optional] |
| **repos** | **Integer** |  | [optional] |
| **public_repos** | **Integer** |  | [optional] |
| **public_gists** | **Integer** |  | [optional] |
| **followers_display_count** | **Integer** |  | [optional] |
| **following_display_count** | **Integer** |  | [optional] |
| **repos_display_count** | **Integer** |  | [optional] |
| **followers_approximate** | **Boolean** |  | [optional] |
| **following_approximate** | **Boolean** |  | [optional] |
| **repos_approximate** | **Boolean** |  | [optional] |
| **starred_count** | **Integer** |  | [optional] |
| **starred_count_approximate** | **Boolean** |  | [optional] |
| **projects_count** | **Integer** |  | [optional] |
| **projects_count_approximate** | **Boolean** |  | [optional] |
| **packages_count** | **Integer** |  | [optional] |
| **packages_count_approximate** | **Boolean** |  | [optional] |
| **sponsoring_count** | **Integer** |  | [optional] |
| **sponsoring_count_approximate** | **Boolean** |  | [optional] |
| **is_sponsorable** | **Boolean** |  | [optional] |
| **sponsors_link** | **String** |  | [optional] |
| **is_verified** | **Boolean** |  | [optional] |
| **has_organization_projects** | **Boolean** |  | [optional] |
| **has_repository_projects** | **Boolean** |  | [optional] |
| **created_at** | **String** |  | [optional] |
| **created_utc** | **Float** |  | [optional] |
| **updated_at** | **String** |  | [optional] |
| **updated_utc** | **Float** |  | [optional] |
| **archived_at** | **String** |  | [optional] |
| **archived_utc** | **Float** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::GitHubProfile.new(
  login: null,
  link: null,
  is_organization: null,
  id: null,
  node_id: null,
  type: null,
  user_view_type: null,
  site_admin: null,
  name: null,
  avatar_url: null,
  bio: null,
  description: null,
  pronouns: null,
  local_time: null,
  utc_offset: null,
  company: null,
  location: null,
  email: null,
  website: null,
  twitter_username: null,
  hireable: null,
  social_accounts: null,
  status: null,
  followers: null,
  following: null,
  repos: null,
  public_repos: null,
  public_gists: null,
  followers_display_count: null,
  following_display_count: null,
  repos_display_count: null,
  followers_approximate: null,
  following_approximate: null,
  repos_approximate: null,
  starred_count: null,
  starred_count_approximate: null,
  projects_count: null,
  projects_count_approximate: null,
  packages_count: null,
  packages_count_approximate: null,
  sponsoring_count: null,
  sponsoring_count_approximate: null,
  is_sponsorable: null,
  sponsors_link: null,
  is_verified: null,
  has_organization_projects: null,
  has_repository_projects: null,
  created_at: null,
  created_utc: null,
  updated_at: null,
  updated_utc: null,
  archived_at: null,
  archived_utc: null
)
```

