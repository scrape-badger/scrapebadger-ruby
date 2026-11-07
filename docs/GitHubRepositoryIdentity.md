# ScrapeBadger::GitHubRepositoryIdentity

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **full_name** | **String** |  |  |
| **link** | **String** |  |  |
| **owner** | [**GitHubRepositoryAccount**](GitHubRepositoryAccount.md) |  |  |
| **is_empty** | **Boolean** |  |  |
| **id** | **Integer** |  | [optional] |
| **node_id** | **String** |  | [optional] |
| **description** | **String** |  | [optional] |
| **website** | **String** |  | [optional] |
| **social_image** | **String** |  | [optional] |
| **default_branch** | **String** |  | [optional] |
| **current_commit** | **String** |  | [optional] |
| **visibility** | **String** |  | [optional] |
| **is_fork** | **Boolean** |  | [optional] |
| **forked_from** | **String** |  | [optional] |
| **parent** | [**GitHubRepositoryReference**](GitHubRepositoryReference.md) |  | [optional] |
| **source** | [**GitHubRepositoryReference**](GitHubRepositoryReference.md) |  | [optional] |
| **fork_comparison** | [**GitHubForkComparison**](GitHubForkComparison.md) |  | [optional] |
| **is_archived** | **Boolean** |  | [optional] |
| **is_template** | **Boolean** |  | [optional] |
| **is_mirror** | **Boolean** |  | [optional] |
| **is_disabled** | **Boolean** |  | [optional] |
| **language** | **String** |  | [optional] |
| **language_color** | **String** |  | [optional] |
| **license** | [**GitHubRepositoryLicense**](GitHubRepositoryLicense.md) |  | [optional] |
| **topics** | **Array&lt;String&gt;** |  | [optional] |
| **stars** | **Integer** |  | [optional] |
| **watchers** | **Integer** |  | [optional] |
| **forks** | **Integer** |  | [optional] |
| **network_count** | **Integer** |  | [optional] |
| **open_issues_count** | **Integer** |  | [optional] |
| **open_pull_requests_count** | **Integer** |  | [optional] |
| **open_issues_count_approximate** | **Boolean** |  | [optional] |
| **open_pull_requests_count_approximate** | **Boolean** |  | [optional] |
| **open_issues_display** | **String** |  | [optional] |
| **open_pull_requests_display** | **String** |  | [optional] |
| **is_open_issues_count_capped** | **Boolean** |  | [optional] |
| **is_open_pull_requests_count_capped** | **Boolean** |  | [optional] |
| **open_issues_and_pull_requests_count** | **Integer** |  | [optional] |
| **commits_count** | **Integer** |  | [optional] |
| **commits_display** | **String** |  | [optional] |
| **commits_count_approximate** | **Boolean** |  | [optional] |
| **branches_count** | **Integer** |  | [optional] |
| **branches_count_approximate** | **Boolean** |  | [optional] |
| **tags_count** | **Integer** |  | [optional] |
| **releases_count** | **Integer** |  | [optional] |
| **contributors_count** | **Integer** |  | [optional] |
| **contributors_count_approximate** | **Boolean** |  | [optional] |
| **used_by_count** | **Integer** |  | [optional] |
| **used_by_count_approximate** | **Boolean** |  | [optional] |
| **security_advisories_count** | **Integer** |  | [optional] |
| **files_count** | **Integer** |  | [optional] |
| **files_truncated** | **Boolean** |  | [optional] |
| **has_issues** | **Boolean** |  | [optional] |
| **has_pull_requests** | **Boolean** |  | [optional] |
| **has_discussions** | **Boolean** |  | [optional] |
| **has_projects** | **Boolean** |  | [optional] |
| **has_wiki** | **Boolean** |  | [optional] |
| **has_pages** | **Boolean** |  | [optional] |
| **has_downloads** | **Boolean** |  | [optional] |
| **has_citation** | **Boolean** |  | [optional] |
| **has_code_of_conduct** | **Boolean** |  | [optional] |
| **has_contributing_guide** | **Boolean** |  | [optional] |
| **has_security_policy** | **Boolean** |  | [optional] |
| **allow_forking** | **Boolean** |  | [optional] |
| **web_commit_signoff_required** | **Boolean** |  | [optional] |
| **pull_request_creation_policy** | **String** |  | [optional] |
| **size_kb** | **Integer** |  | [optional] |
| **clone_url** | **String** |  | [optional] |
| **ssh_url** | **String** |  | [optional] |
| **git_url** | **String** |  | [optional] |
| **svn_url** | **String** |  | [optional] |
| **archive_url** | **String** |  | [optional] |
| **mirror_url** | **String** |  | [optional] |
| **created_at** | **String** |  | [optional] |
| **created_utc** | **Float** |  | [optional] |
| **updated_at** | **String** |  | [optional] |
| **updated_utc** | **Float** |  | [optional] |
| **pushed_at** | **String** |  | [optional] |
| **pushed_utc** | **Float** |  | [optional] |

## Example

```ruby
require 'scrapebadger'

instance = ScrapeBadger::GitHubRepositoryIdentity.new(
  name: null,
  full_name: null,
  link: null,
  owner: null,
  is_empty: null,
  id: null,
  node_id: null,
  description: null,
  website: null,
  social_image: null,
  default_branch: null,
  current_commit: null,
  visibility: null,
  is_fork: null,
  forked_from: null,
  parent: null,
  source: null,
  fork_comparison: null,
  is_archived: null,
  is_template: null,
  is_mirror: null,
  is_disabled: null,
  language: null,
  language_color: null,
  license: null,
  topics: null,
  stars: null,
  watchers: null,
  forks: null,
  network_count: null,
  open_issues_count: null,
  open_pull_requests_count: null,
  open_issues_count_approximate: null,
  open_pull_requests_count_approximate: null,
  open_issues_display: null,
  open_pull_requests_display: null,
  is_open_issues_count_capped: null,
  is_open_pull_requests_count_capped: null,
  open_issues_and_pull_requests_count: null,
  commits_count: null,
  commits_display: null,
  commits_count_approximate: null,
  branches_count: null,
  branches_count_approximate: null,
  tags_count: null,
  releases_count: null,
  contributors_count: null,
  contributors_count_approximate: null,
  used_by_count: null,
  used_by_count_approximate: null,
  security_advisories_count: null,
  files_count: null,
  files_truncated: null,
  has_issues: null,
  has_pull_requests: null,
  has_discussions: null,
  has_projects: null,
  has_wiki: null,
  has_pages: null,
  has_downloads: null,
  has_citation: null,
  has_code_of_conduct: null,
  has_contributing_guide: null,
  has_security_policy: null,
  allow_forking: null,
  web_commit_signoff_required: null,
  pull_request_creation_policy: null,
  size_kb: null,
  clone_url: null,
  ssh_url: null,
  git_url: null,
  svn_url: null,
  archive_url: null,
  mirror_url: null,
  created_at: null,
  created_utc: null,
  updated_at: null,
  updated_utc: null,
  pushed_at: null,
  pushed_utc: null
)
```

