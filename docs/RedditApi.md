# ScrapeBadger::RedditApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**reddit_get_cross_posts**](RedditApi.md#reddit_get_cross_posts) | **GET** /v1/reddit/posts/{post_id}/duplicates | Get cross-posts |
| [**reddit_get_post_comments**](RedditApi.md#reddit_get_post_comments) | **GET** /v1/reddit/posts/{post_id}/comments | Get post comments |
| [**reddit_get_post_detail**](RedditApi.md#reddit_get_post_detail) | **GET** /v1/reddit/posts/{post_id} | Get post detail |
| [**reddit_get_posts_by_domain**](RedditApi.md#reddit_get_posts_by_domain) | **GET** /v1/reddit/domains/{domain}/posts | Get posts by domain |
| [**reddit_get_subreddit_info**](RedditApi.md#reddit_get_subreddit_info) | **GET** /v1/reddit/subreddits/{subreddit} | Get subreddit info |
| [**reddit_get_subreddit_posts**](RedditApi.md#reddit_get_subreddit_posts) | **GET** /v1/reddit/subreddits/{subreddit}/posts | Get subreddit posts |
| [**reddit_get_subreddit_rules**](RedditApi.md#reddit_get_subreddit_rules) | **GET** /v1/reddit/subreddits/{subreddit}/rules | Get subreddit rules |
| [**reddit_get_trending_posts**](RedditApi.md#reddit_get_trending_posts) | **GET** /v1/reddit/posts/trending | Get trending posts |
| [**reddit_get_user_profile**](RedditApi.md#reddit_get_user_profile) | **GET** /v1/reddit/users/{username} | Get user profile |
| [**reddit_get_user_s_comments**](RedditApi.md#reddit_get_user_s_comments) | **GET** /v1/reddit/users/{username}/comments | Get user&#39;s comments |
| [**reddit_get_user_s_moderated_subreddits**](RedditApi.md#reddit_get_user_s_moderated_subreddits) | **GET** /v1/reddit/users/{username}/moderated | Get user&#39;s moderated subreddits |
| [**reddit_get_user_s_posts**](RedditApi.md#reddit_get_user_s_posts) | **GET** /v1/reddit/users/{username}/posts | Get user&#39;s posts |
| [**reddit_get_user_s_trophies**](RedditApi.md#reddit_get_user_s_trophies) | **GET** /v1/reddit/users/{username}/trophies | Get user&#39;s trophies |
| [**reddit_get_wiki_page_content**](RedditApi.md#reddit_get_wiki_page_content) | **GET** /v1/reddit/subreddits/{subreddit}/wiki/{page} | Get wiki page content |
| [**reddit_list_wiki_pages**](RedditApi.md#reddit_list_wiki_pages) | **GET** /v1/reddit/subreddits/{subreddit}/wiki | List wiki pages |
| [**reddit_new_subreddits**](RedditApi.md#reddit_new_subreddits) | **GET** /v1/reddit/subreddits/new | New subreddits |
| [**reddit_popular_subreddits**](RedditApi.md#reddit_popular_subreddits) | **GET** /v1/reddit/subreddits/popular | Popular subreddits |
| [**reddit_reddit_scraper_health_check**](RedditApi.md#reddit_reddit_scraper_health_check) | **GET** /v1/reddit/health | Reddit scraper health check |
| [**reddit_reddit_scraper_health_check_head**](RedditApi.md#reddit_reddit_scraper_health_check_head) | **HEAD** /v1/reddit/health | Reddit scraper health check |
| [**reddit_search_reddit_posts**](RedditApi.md#reddit_search_reddit_posts) | **GET** /v1/reddit/search/posts | Search Reddit posts |
| [**reddit_search_subreddits**](RedditApi.md#reddit_search_subreddits) | **GET** /v1/reddit/search/subreddits | Search subreddits |
| [**reddit_search_users**](RedditApi.md#reddit_search_users) | **GET** /v1/reddit/search/users | Search users |


## reddit_get_cross_posts

> Object reddit_get_cross_posts(post_id, opts)

Get cross-posts

Get cross-posts and duplicates of a Reddit post.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new
post_id = 'post_id_example' # String | 
opts = {
  limit: 56, # Integer | 
  after: 'after_example' # String | 
}

begin
  # Get cross-posts
  result = api_instance.reddit_get_cross_posts(post_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_cross_posts: #{e}"
end
```

#### Using the reddit_get_cross_posts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_get_cross_posts_with_http_info(post_id, opts)

```ruby
begin
  # Get cross-posts
  data, status_code, headers = api_instance.reddit_get_cross_posts_with_http_info(post_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_cross_posts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** |  |  |
| **limit** | **Integer** |  | [optional][default to 25] |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_get_post_comments

> Object reddit_get_post_comments(post_id, opts)

Get post comments

Get comment tree for a Reddit post.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new
post_id = 'post_id_example' # String | 
opts = {
  sort: 'sort_example', # String | Sort: confidence, top, new, controversial, old, qa
  limit: 56, # Integer | 
  depth: 56 # Integer | 
}

begin
  # Get post comments
  result = api_instance.reddit_get_post_comments(post_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_post_comments: #{e}"
end
```

#### Using the reddit_get_post_comments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_get_post_comments_with_http_info(post_id, opts)

```ruby
begin
  # Get post comments
  data, status_code, headers = api_instance.reddit_get_post_comments_with_http_info(post_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_post_comments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** |  |  |
| **sort** | **String** | Sort: confidence, top, new, controversial, old, qa | [optional][default to &#39;confidence&#39;] |
| **limit** | **Integer** |  | [optional][default to 25] |
| **depth** | **Integer** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_get_post_detail

> Object reddit_get_post_detail(post_id)

Get post detail

Get detailed information about a Reddit post.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new
post_id = 'post_id_example' # String | 

begin
  # Get post detail
  result = api_instance.reddit_get_post_detail(post_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_post_detail: #{e}"
end
```

#### Using the reddit_get_post_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_get_post_detail_with_http_info(post_id)

```ruby
begin
  # Get post detail
  data, status_code, headers = api_instance.reddit_get_post_detail_with_http_info(post_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_post_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_get_posts_by_domain

> Object reddit_get_posts_by_domain(domain, opts)

Get posts by domain

Get Reddit posts linking to a specific domain.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new
domain = 'domain_example' # String | 
opts = {
  sort: 'sort_example', # String | 
  t: 't_example', # String | 
  limit: 56, # Integer | 
  after: 'after_example' # String | 
}

begin
  # Get posts by domain
  result = api_instance.reddit_get_posts_by_domain(domain, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_posts_by_domain: #{e}"
end
```

#### Using the reddit_get_posts_by_domain_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_get_posts_by_domain_with_http_info(domain, opts)

```ruby
begin
  # Get posts by domain
  data, status_code, headers = api_instance.reddit_get_posts_by_domain_with_http_info(domain, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_posts_by_domain_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **domain** | **String** |  |  |
| **sort** | **String** |  | [optional][default to &#39;hot&#39;] |
| **t** | **String** |  | [optional][default to &#39;all&#39;] |
| **limit** | **Integer** |  | [optional][default to 25] |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_get_subreddit_info

> Object reddit_get_subreddit_info(subreddit)

Get subreddit info

Get detailed information about a subreddit.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new
subreddit = 'subreddit_example' # String | 

begin
  # Get subreddit info
  result = api_instance.reddit_get_subreddit_info(subreddit)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_subreddit_info: #{e}"
end
```

#### Using the reddit_get_subreddit_info_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_get_subreddit_info_with_http_info(subreddit)

```ruby
begin
  # Get subreddit info
  data, status_code, headers = api_instance.reddit_get_subreddit_info_with_http_info(subreddit)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_subreddit_info_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subreddit** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_get_subreddit_posts

> Object reddit_get_subreddit_posts(subreddit, opts)

Get subreddit posts

Get posts from a subreddit with sorting options.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new
subreddit = 'subreddit_example' # String | 
opts = {
  sort: 'sort_example', # String | Sort: hot, new, top, rising, controversial
  t: 't_example', # String | Time filter
  limit: 56, # Integer | 
  after: 'after_example' # String | 
}

begin
  # Get subreddit posts
  result = api_instance.reddit_get_subreddit_posts(subreddit, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_subreddit_posts: #{e}"
end
```

#### Using the reddit_get_subreddit_posts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_get_subreddit_posts_with_http_info(subreddit, opts)

```ruby
begin
  # Get subreddit posts
  data, status_code, headers = api_instance.reddit_get_subreddit_posts_with_http_info(subreddit, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_subreddit_posts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subreddit** | **String** |  |  |
| **sort** | **String** | Sort: hot, new, top, rising, controversial | [optional][default to &#39;hot&#39;] |
| **t** | **String** | Time filter | [optional][default to &#39;all&#39;] |
| **limit** | **Integer** |  | [optional][default to 25] |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_get_subreddit_rules

> Object reddit_get_subreddit_rules(subreddit)

Get subreddit rules

Get the rules of a subreddit.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new
subreddit = 'subreddit_example' # String | 

begin
  # Get subreddit rules
  result = api_instance.reddit_get_subreddit_rules(subreddit)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_subreddit_rules: #{e}"
end
```

#### Using the reddit_get_subreddit_rules_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_get_subreddit_rules_with_http_info(subreddit)

```ruby
begin
  # Get subreddit rules
  data, status_code, headers = api_instance.reddit_get_subreddit_rules_with_http_info(subreddit)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_subreddit_rules_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subreddit** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_get_trending_posts

> Object reddit_get_trending_posts(opts)

Get trending posts

Get trending posts from Reddit's front page.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new
opts = {
  sort: 'sort_example', # String | Sort: hot, new, top, rising, controversial, best
  t: 't_example', # String | Time filter
  limit: 56, # Integer | 
  after: 'after_example' # String | 
}

begin
  # Get trending posts
  result = api_instance.reddit_get_trending_posts(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_trending_posts: #{e}"
end
```

#### Using the reddit_get_trending_posts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_get_trending_posts_with_http_info(opts)

```ruby
begin
  # Get trending posts
  data, status_code, headers = api_instance.reddit_get_trending_posts_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_trending_posts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sort** | **String** | Sort: hot, new, top, rising, controversial, best | [optional][default to &#39;hot&#39;] |
| **t** | **String** | Time filter | [optional][default to &#39;day&#39;] |
| **limit** | **Integer** |  | [optional][default to 25] |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_get_user_profile

> Object reddit_get_user_profile(username)

Get user profile

Get a Reddit user's profile.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new
username = 'username_example' # String | 

begin
  # Get user profile
  result = api_instance.reddit_get_user_profile(username)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_user_profile: #{e}"
end
```

#### Using the reddit_get_user_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_get_user_profile_with_http_info(username)

```ruby
begin
  # Get user profile
  data, status_code, headers = api_instance.reddit_get_user_profile_with_http_info(username)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_user_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_get_user_s_comments

> Object reddit_get_user_s_comments(username, opts)

Get user's comments

Get comments by a Reddit user.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new
username = 'username_example' # String | 
opts = {
  sort: 'sort_example', # String | 
  t: 't_example', # String | 
  limit: 56, # Integer | 
  after: 'after_example' # String | 
}

begin
  # Get user's comments
  result = api_instance.reddit_get_user_s_comments(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_user_s_comments: #{e}"
end
```

#### Using the reddit_get_user_s_comments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_get_user_s_comments_with_http_info(username, opts)

```ruby
begin
  # Get user's comments
  data, status_code, headers = api_instance.reddit_get_user_s_comments_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_user_s_comments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **sort** | **String** |  | [optional][default to &#39;new&#39;] |
| **t** | **String** |  | [optional][default to &#39;all&#39;] |
| **limit** | **Integer** |  | [optional][default to 25] |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_get_user_s_moderated_subreddits

> Object reddit_get_user_s_moderated_subreddits(username)

Get user's moderated subreddits

Get subreddits moderated by a user.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new
username = 'username_example' # String | 

begin
  # Get user's moderated subreddits
  result = api_instance.reddit_get_user_s_moderated_subreddits(username)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_user_s_moderated_subreddits: #{e}"
end
```

#### Using the reddit_get_user_s_moderated_subreddits_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_get_user_s_moderated_subreddits_with_http_info(username)

```ruby
begin
  # Get user's moderated subreddits
  data, status_code, headers = api_instance.reddit_get_user_s_moderated_subreddits_with_http_info(username)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_user_s_moderated_subreddits_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_get_user_s_posts

> Object reddit_get_user_s_posts(username, opts)

Get user's posts

Get posts submitted by a Reddit user.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new
username = 'username_example' # String | 
opts = {
  sort: 'sort_example', # String | 
  t: 't_example', # String | 
  limit: 56, # Integer | 
  after: 'after_example' # String | 
}

begin
  # Get user's posts
  result = api_instance.reddit_get_user_s_posts(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_user_s_posts: #{e}"
end
```

#### Using the reddit_get_user_s_posts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_get_user_s_posts_with_http_info(username, opts)

```ruby
begin
  # Get user's posts
  data, status_code, headers = api_instance.reddit_get_user_s_posts_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_user_s_posts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **sort** | **String** |  | [optional][default to &#39;new&#39;] |
| **t** | **String** |  | [optional][default to &#39;all&#39;] |
| **limit** | **Integer** |  | [optional][default to 25] |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_get_user_s_trophies

> Object reddit_get_user_s_trophies(username)

Get user's trophies

Get a user's trophy case.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new
username = 'username_example' # String | 

begin
  # Get user's trophies
  result = api_instance.reddit_get_user_s_trophies(username)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_user_s_trophies: #{e}"
end
```

#### Using the reddit_get_user_s_trophies_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_get_user_s_trophies_with_http_info(username)

```ruby
begin
  # Get user's trophies
  data, status_code, headers = api_instance.reddit_get_user_s_trophies_with_http_info(username)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_user_s_trophies_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_get_wiki_page_content

> Object reddit_get_wiki_page_content(subreddit, page)

Get wiki page content

Get the content of a specific wiki page.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new
subreddit = 'subreddit_example' # String | 
page = 'page_example' # String | 

begin
  # Get wiki page content
  result = api_instance.reddit_get_wiki_page_content(subreddit, page)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_wiki_page_content: #{e}"
end
```

#### Using the reddit_get_wiki_page_content_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_get_wiki_page_content_with_http_info(subreddit, page)

```ruby
begin
  # Get wiki page content
  data, status_code, headers = api_instance.reddit_get_wiki_page_content_with_http_info(subreddit, page)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_get_wiki_page_content_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subreddit** | **String** |  |  |
| **page** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_list_wiki_pages

> Object reddit_list_wiki_pages(subreddit)

List wiki pages

List all wiki pages in a subreddit.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new
subreddit = 'subreddit_example' # String | 

begin
  # List wiki pages
  result = api_instance.reddit_list_wiki_pages(subreddit)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_list_wiki_pages: #{e}"
end
```

#### Using the reddit_list_wiki_pages_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_list_wiki_pages_with_http_info(subreddit)

```ruby
begin
  # List wiki pages
  data, status_code, headers = api_instance.reddit_list_wiki_pages_with_http_info(subreddit)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_list_wiki_pages_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subreddit** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_new_subreddits

> Object reddit_new_subreddits(opts)

New subreddits

Get recently created subreddits.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new
opts = {
  limit: 56, # Integer | 
  after: 'after_example' # String | 
}

begin
  # New subreddits
  result = api_instance.reddit_new_subreddits(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_new_subreddits: #{e}"
end
```

#### Using the reddit_new_subreddits_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_new_subreddits_with_http_info(opts)

```ruby
begin
  # New subreddits
  data, status_code, headers = api_instance.reddit_new_subreddits_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_new_subreddits_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** |  | [optional][default to 25] |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_popular_subreddits

> Object reddit_popular_subreddits(opts)

Popular subreddits

Get popular subreddits by subscriber count.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new
opts = {
  limit: 56, # Integer | 
  after: 'after_example' # String | 
}

begin
  # Popular subreddits
  result = api_instance.reddit_popular_subreddits(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_popular_subreddits: #{e}"
end
```

#### Using the reddit_popular_subreddits_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_popular_subreddits_with_http_info(opts)

```ruby
begin
  # Popular subreddits
  data, status_code, headers = api_instance.reddit_popular_subreddits_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_popular_subreddits_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** |  | [optional][default to 25] |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_reddit_scraper_health_check

> Object reddit_reddit_scraper_health_check

Reddit scraper health check

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new

begin
  # Reddit scraper health check
  result = api_instance.reddit_reddit_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_reddit_scraper_health_check: #{e}"
end
```

#### Using the reddit_reddit_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_reddit_scraper_health_check_with_http_info

```ruby
begin
  # Reddit scraper health check
  data, status_code, headers = api_instance.reddit_reddit_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_reddit_scraper_health_check_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_reddit_scraper_health_check_head

> Object reddit_reddit_scraper_health_check_head

Reddit scraper health check

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new

begin
  # Reddit scraper health check
  result = api_instance.reddit_reddit_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_reddit_scraper_health_check_head: #{e}"
end
```

#### Using the reddit_reddit_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_reddit_scraper_health_check_head_with_http_info

```ruby
begin
  # Reddit scraper health check
  data, status_code, headers = api_instance.reddit_reddit_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_reddit_scraper_health_check_head_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_search_reddit_posts

> Object reddit_search_reddit_posts(q, opts)

Search Reddit posts

Search Reddit posts globally or within a subreddit.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new
q = 'q_example' # String | Search query
opts = {
  subreddit: 'subreddit_example', # String | Restrict to subreddit
  sort: 'sort_example', # String | Sort: relevance, hot, top, new, comments
  t: 't_example', # String | Time: hour, day, week, month, year, all
  limit: 56, # Integer | 
  after: 'after_example' # String | 
}

begin
  # Search Reddit posts
  result = api_instance.reddit_search_reddit_posts(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_search_reddit_posts: #{e}"
end
```

#### Using the reddit_search_reddit_posts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_search_reddit_posts_with_http_info(q, opts)

```ruby
begin
  # Search Reddit posts
  data, status_code, headers = api_instance.reddit_search_reddit_posts_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_search_reddit_posts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Search query |  |
| **subreddit** | **String** | Restrict to subreddit | [optional] |
| **sort** | **String** | Sort: relevance, hot, top, new, comments | [optional][default to &#39;relevance&#39;] |
| **t** | **String** | Time: hour, day, week, month, year, all | [optional][default to &#39;all&#39;] |
| **limit** | **Integer** |  | [optional][default to 25] |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_search_subreddits

> Object reddit_search_subreddits(q, opts)

Search subreddits

Search for subreddits by keyword.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new
q = 'q_example' # String | Search query
opts = {
  limit: 56, # Integer | 
  after: 'after_example' # String | 
}

begin
  # Search subreddits
  result = api_instance.reddit_search_subreddits(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_search_subreddits: #{e}"
end
```

#### Using the reddit_search_subreddits_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_search_subreddits_with_http_info(q, opts)

```ruby
begin
  # Search subreddits
  data, status_code, headers = api_instance.reddit_search_subreddits_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_search_subreddits_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Search query |  |
| **limit** | **Integer** |  | [optional][default to 25] |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reddit_search_users

> Object reddit_search_users(q, opts)

Search users

Search for Reddit users.

### Examples

```ruby
require 'time'
require 'scrapebadger'
# setup authorization
ScrapeBadger.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['X-API-Key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['X-API-Key'] = 'Bearer'
end

api_instance = ScrapeBadger::RedditApi.new
q = 'q_example' # String | Search query
opts = {
  limit: 56, # Integer | 
  after: 'after_example' # String | 
}

begin
  # Search users
  result = api_instance.reddit_search_users(q, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_search_users: #{e}"
end
```

#### Using the reddit_search_users_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> reddit_search_users_with_http_info(q, opts)

```ruby
begin
  # Search users
  data, status_code, headers = api_instance.reddit_search_users_with_http_info(q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling RedditApi->reddit_search_users_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** | Search query |  |
| **limit** | **Integer** |  | [optional][default to 25] |
| **after** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

