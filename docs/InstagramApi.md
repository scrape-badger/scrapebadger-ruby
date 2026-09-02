# ScrapeBadger::InstagramApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**instagram_about_this_account**](InstagramApi.md#instagram_about_this_account) | **GET** /v1/instagram/users/{username}/about | About this account |
| [**instagram_blended_top_search**](InstagramApi.md#instagram_blended_top_search) | **GET** /v1/instagram/search/top | Blended top search |
| [**instagram_get_active_stories**](InstagramApi.md#instagram_get_active_stories) | **GET** /v1/instagram/users/{username}/stories | Get active stories |
| [**instagram_get_audio_track**](InstagramApi.md#instagram_get_audio_track) | **GET** /v1/instagram/audio/{audio_id} | Get audio track |
| [**instagram_get_comments**](InstagramApi.md#instagram_get_comments) | **GET** /v1/instagram/media/{code}/comments | Get comments |
| [**instagram_get_followers**](InstagramApi.md#instagram_get_followers) | **GET** /v1/instagram/users/{username}/followers | Get followers |
| [**instagram_get_following**](InstagramApi.md#instagram_get_following) | **GET** /v1/instagram/users/{username}/following | Get following |
| [**instagram_get_hashtag_info**](InstagramApi.md#instagram_get_hashtag_info) | **GET** /v1/instagram/hashtags/{tag} | Get hashtag info |
| [**instagram_get_highlights**](InstagramApi.md#instagram_get_highlights) | **GET** /v1/instagram/users/{username}/highlights | Get highlights |
| [**instagram_get_likers**](InstagramApi.md#instagram_get_likers) | **GET** /v1/instagram/media/{code}/likers | Get likers |
| [**instagram_get_location**](InstagramApi.md#instagram_get_location) | **GET** /v1/instagram/locations/{location_pk} | Get location |
| [**instagram_get_post_reel_detail**](InstagramApi.md#instagram_get_post_reel_detail) | **GET** /v1/instagram/media/{code} | Get post/reel detail |
| [**instagram_get_profile**](InstagramApi.md#instagram_get_profile) | **GET** /v1/instagram/users/{username} | Get profile |
| [**instagram_get_tagged_posts**](InstagramApi.md#instagram_get_tagged_posts) | **GET** /v1/instagram/users/{username}/tagged | Get tagged posts |
| [**instagram_get_user_posts**](InstagramApi.md#instagram_get_user_posts) | **GET** /v1/instagram/users/{username}/posts | Get user posts |
| [**instagram_get_user_reels**](InstagramApi.md#instagram_get_user_reels) | **GET** /v1/instagram/users/{username}/reels | Get user reels |
| [**instagram_health**](InstagramApi.md#instagram_health) | **GET** /v1/instagram/health | Health |
| [**instagram_health_head**](InstagramApi.md#instagram_health_head) | **HEAD** /v1/instagram/health | Health |
| [**instagram_recent_hashtag_posts**](InstagramApi.md#instagram_recent_hashtag_posts) | **GET** /v1/instagram/hashtags/{tag}/recent | Recent hashtag posts |
| [**instagram_related_profiles**](InstagramApi.md#instagram_related_profiles) | **GET** /v1/instagram/users/{username}/related | Related profiles |
| [**instagram_search_hashtags**](InstagramApi.md#instagram_search_hashtags) | **GET** /v1/instagram/search/hashtags | Search hashtags |
| [**instagram_search_users**](InstagramApi.md#instagram_search_users) | **GET** /v1/instagram/search/users | Search users |
| [**instagram_top_hashtag_posts**](InstagramApi.md#instagram_top_hashtag_posts) | **GET** /v1/instagram/hashtags/{tag}/top | Top hashtag posts |


## instagram_about_this_account

> Object instagram_about_this_account(username)

About this account

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns `503 temporarily_unavailable` (not billed, `Retry-After` set) — see https://docs.scrapebadger.com/instagram/overview. Country, join date and former usernames.

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

api_instance = ScrapeBadger::InstagramApi.new
username = 'username_example' # String | 

begin
  # About this account
  result = api_instance.instagram_about_this_account(username)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_about_this_account: #{e}"
end
```

#### Using the instagram_about_this_account_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_about_this_account_with_http_info(username)

```ruby
begin
  # About this account
  data, status_code, headers = api_instance.instagram_about_this_account_with_http_info(username)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_about_this_account_with_http_info: #{e}"
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


## instagram_blended_top_search

> Object instagram_blended_top_search(query)

Blended top search

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns `503 temporarily_unavailable` (not billed, `Retry-After` set) — see https://docs.scrapebadger.com/instagram/overview.

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

api_instance = ScrapeBadger::InstagramApi.new
query = 'query_example' # String | 

begin
  # Blended top search
  result = api_instance.instagram_blended_top_search(query)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_blended_top_search: #{e}"
end
```

#### Using the instagram_blended_top_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_blended_top_search_with_http_info(query)

```ruby
begin
  # Blended top search
  data, status_code, headers = api_instance.instagram_blended_top_search_with_http_info(query)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_blended_top_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## instagram_get_active_stories

> Object instagram_get_active_stories(username)

Get active stories

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns `503 temporarily_unavailable` (not billed, `Retry-After` set) — see https://docs.scrapebadger.com/instagram/overview. Active stories (account pool only).

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

api_instance = ScrapeBadger::InstagramApi.new
username = 'username_example' # String | 

begin
  # Get active stories
  result = api_instance.instagram_get_active_stories(username)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_active_stories: #{e}"
end
```

#### Using the instagram_get_active_stories_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_get_active_stories_with_http_info(username)

```ruby
begin
  # Get active stories
  data, status_code, headers = api_instance.instagram_get_active_stories_with_http_info(username)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_active_stories_with_http_info: #{e}"
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


## instagram_get_audio_track

> Object instagram_get_audio_track(audio_id)

Get audio track

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns `503 temporarily_unavailable` (not billed, `Retry-After` set) — see https://docs.scrapebadger.com/instagram/overview.

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

api_instance = ScrapeBadger::InstagramApi.new
audio_id = 'audio_id_example' # String | 

begin
  # Get audio track
  result = api_instance.instagram_get_audio_track(audio_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_audio_track: #{e}"
end
```

#### Using the instagram_get_audio_track_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_get_audio_track_with_http_info(audio_id)

```ruby
begin
  # Get audio track
  data, status_code, headers = api_instance.instagram_get_audio_track_with_http_info(audio_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_audio_track_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **audio_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## instagram_get_comments

> Object instagram_get_comments(code, opts)

Get comments

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

api_instance = ScrapeBadger::InstagramApi.new
code = 'code_example' # String | 
opts = {
  amount: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # Get comments
  result = api_instance.instagram_get_comments(code, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_comments: #{e}"
end
```

#### Using the instagram_get_comments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_get_comments_with_http_info(code, opts)

```ruby
begin
  # Get comments
  data, status_code, headers = api_instance.instagram_get_comments_with_http_info(code, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_comments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** |  |  |
| **amount** | **Integer** |  | [optional][default to 20] |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## instagram_get_followers

> Object instagram_get_followers(username, opts)

Get followers

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns `503 temporarily_unavailable` (not billed, `Retry-After` set) — see https://docs.scrapebadger.com/instagram/overview. Followers list, paginated (account pool).

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

api_instance = ScrapeBadger::InstagramApi.new
username = 'username_example' # String | 
opts = {
  amount: 56, # Integer | 
  cursor: 'cursor_example', # String | 
  order: 'order_example' # String | date_followed_latest | date_followed_earliest
}

begin
  # Get followers
  result = api_instance.instagram_get_followers(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_followers: #{e}"
end
```

#### Using the instagram_get_followers_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_get_followers_with_http_info(username, opts)

```ruby
begin
  # Get followers
  data, status_code, headers = api_instance.instagram_get_followers_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_followers_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **amount** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |
| **order** | **String** | date_followed_latest | date_followed_earliest | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## instagram_get_following

> Object instagram_get_following(username, opts)

Get following

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns `503 temporarily_unavailable` (not billed, `Retry-After` set) — see https://docs.scrapebadger.com/instagram/overview.

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

api_instance = ScrapeBadger::InstagramApi.new
username = 'username_example' # String | 
opts = {
  amount: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # Get following
  result = api_instance.instagram_get_following(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_following: #{e}"
end
```

#### Using the instagram_get_following_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_get_following_with_http_info(username, opts)

```ruby
begin
  # Get following
  data, status_code, headers = api_instance.instagram_get_following_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_following_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **amount** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## instagram_get_hashtag_info

> Object instagram_get_hashtag_info(tag)

Get hashtag info

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns `503 temporarily_unavailable` (not billed, `Retry-After` set) — see https://docs.scrapebadger.com/instagram/overview.

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

api_instance = ScrapeBadger::InstagramApi.new
tag = 'tag_example' # String | 

begin
  # Get hashtag info
  result = api_instance.instagram_get_hashtag_info(tag)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_hashtag_info: #{e}"
end
```

#### Using the instagram_get_hashtag_info_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_get_hashtag_info_with_http_info(tag)

```ruby
begin
  # Get hashtag info
  data, status_code, headers = api_instance.instagram_get_hashtag_info_with_http_info(tag)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_hashtag_info_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tag** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## instagram_get_highlights

> Object instagram_get_highlights(username)

Get highlights

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns `503 temporarily_unavailable` (not billed, `Retry-After` set) — see https://docs.scrapebadger.com/instagram/overview.

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

api_instance = ScrapeBadger::InstagramApi.new
username = 'username_example' # String | 

begin
  # Get highlights
  result = api_instance.instagram_get_highlights(username)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_highlights: #{e}"
end
```

#### Using the instagram_get_highlights_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_get_highlights_with_http_info(username)

```ruby
begin
  # Get highlights
  data, status_code, headers = api_instance.instagram_get_highlights_with_http_info(username)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_highlights_with_http_info: #{e}"
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


## instagram_get_likers

> Object instagram_get_likers(code)

Get likers

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns `503 temporarily_unavailable` (not billed, `Retry-After` set) — see https://docs.scrapebadger.com/instagram/overview.

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

api_instance = ScrapeBadger::InstagramApi.new
code = 'code_example' # String | 

begin
  # Get likers
  result = api_instance.instagram_get_likers(code)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_likers: #{e}"
end
```

#### Using the instagram_get_likers_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_get_likers_with_http_info(code)

```ruby
begin
  # Get likers
  data, status_code, headers = api_instance.instagram_get_likers_with_http_info(code)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_likers_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## instagram_get_location

> Object instagram_get_location(location_pk)

Get location

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns `503 temporarily_unavailable` (not billed, `Retry-After` set) — see https://docs.scrapebadger.com/instagram/overview.

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

api_instance = ScrapeBadger::InstagramApi.new
location_pk = 56 # Integer | 

begin
  # Get location
  result = api_instance.instagram_get_location(location_pk)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_location: #{e}"
end
```

#### Using the instagram_get_location_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_get_location_with_http_info(location_pk)

```ruby
begin
  # Get location
  data, status_code, headers = api_instance.instagram_get_location_with_http_info(location_pk)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_location_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **location_pk** | **Integer** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## instagram_get_post_reel_detail

> Object instagram_get_post_reel_detail(code)

Get post/reel detail

Single post or reel: caption, media, counts, tags, location, carousel.

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

api_instance = ScrapeBadger::InstagramApi.new
code = 'code_example' # String | 

begin
  # Get post/reel detail
  result = api_instance.instagram_get_post_reel_detail(code)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_post_reel_detail: #{e}"
end
```

#### Using the instagram_get_post_reel_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_get_post_reel_detail_with_http_info(code)

```ruby
begin
  # Get post/reel detail
  data, status_code, headers = api_instance.instagram_get_post_reel_detail_with_http_info(code)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_post_reel_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## instagram_get_profile

> Object instagram_get_profile(username)

Get profile

Full public profile: bio, counts, verification, business contact, links.

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

api_instance = ScrapeBadger::InstagramApi.new
username = 'username_example' # String | 

begin
  # Get profile
  result = api_instance.instagram_get_profile(username)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_profile: #{e}"
end
```

#### Using the instagram_get_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_get_profile_with_http_info(username)

```ruby
begin
  # Get profile
  data, status_code, headers = api_instance.instagram_get_profile_with_http_info(username)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_profile_with_http_info: #{e}"
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


## instagram_get_tagged_posts

> Object instagram_get_tagged_posts(username, opts)

Get tagged posts

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns `503 temporarily_unavailable` (not billed, `Retry-After` set) — see https://docs.scrapebadger.com/instagram/overview.

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

api_instance = ScrapeBadger::InstagramApi.new
username = 'username_example' # String | 
opts = {
  amount: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # Get tagged posts
  result = api_instance.instagram_get_tagged_posts(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_tagged_posts: #{e}"
end
```

#### Using the instagram_get_tagged_posts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_get_tagged_posts_with_http_info(username, opts)

```ruby
begin
  # Get tagged posts
  data, status_code, headers = api_instance.instagram_get_tagged_posts_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_tagged_posts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **amount** | **Integer** |  | [optional][default to 20] |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## instagram_get_user_posts

> Object instagram_get_user_posts(username, opts)

Get user posts

Timeline posts, paginated.

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

api_instance = ScrapeBadger::InstagramApi.new
username = 'username_example' # String | 
opts = {
  amount: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # Get user posts
  result = api_instance.instagram_get_user_posts(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_user_posts: #{e}"
end
```

#### Using the instagram_get_user_posts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_get_user_posts_with_http_info(username, opts)

```ruby
begin
  # Get user posts
  data, status_code, headers = api_instance.instagram_get_user_posts_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_user_posts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **amount** | **Integer** |  | [optional][default to 20] |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## instagram_get_user_reels

> Object instagram_get_user_reels(username, opts)

Get user reels

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns `503 temporarily_unavailable` (not billed, `Retry-After` set) — see https://docs.scrapebadger.com/instagram/overview.

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

api_instance = ScrapeBadger::InstagramApi.new
username = 'username_example' # String | 
opts = {
  amount: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # Get user reels
  result = api_instance.instagram_get_user_reels(username, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_user_reels: #{e}"
end
```

#### Using the instagram_get_user_reels_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_get_user_reels_with_http_info(username, opts)

```ruby
begin
  # Get user reels
  data, status_code, headers = api_instance.instagram_get_user_reels_with_http_info(username, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_get_user_reels_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** |  |  |
| **amount** | **Integer** |  | [optional][default to 20] |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## instagram_health

> Object instagram_health

Health

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

api_instance = ScrapeBadger::InstagramApi.new

begin
  # Health
  result = api_instance.instagram_health
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_health: #{e}"
end
```

#### Using the instagram_health_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_health_with_http_info

```ruby
begin
  # Health
  data, status_code, headers = api_instance.instagram_health_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_health_with_http_info: #{e}"
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


## instagram_health_head

> Object instagram_health_head

Health

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

api_instance = ScrapeBadger::InstagramApi.new

begin
  # Health
  result = api_instance.instagram_health_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_health_head: #{e}"
end
```

#### Using the instagram_health_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_health_head_with_http_info

```ruby
begin
  # Health
  data, status_code, headers = api_instance.instagram_health_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_health_head_with_http_info: #{e}"
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


## instagram_recent_hashtag_posts

> Object instagram_recent_hashtag_posts(tag, opts)

Recent hashtag posts

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns `503 temporarily_unavailable` (not billed, `Retry-After` set) — see https://docs.scrapebadger.com/instagram/overview.

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

api_instance = ScrapeBadger::InstagramApi.new
tag = 'tag_example' # String | 
opts = {
  amount: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # Recent hashtag posts
  result = api_instance.instagram_recent_hashtag_posts(tag, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_recent_hashtag_posts: #{e}"
end
```

#### Using the instagram_recent_hashtag_posts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_recent_hashtag_posts_with_http_info(tag, opts)

```ruby
begin
  # Recent hashtag posts
  data, status_code, headers = api_instance.instagram_recent_hashtag_posts_with_http_info(tag, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_recent_hashtag_posts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tag** | **String** |  |  |
| **amount** | **Integer** |  | [optional][default to 20] |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## instagram_related_profiles

> Object instagram_related_profiles(username)

Related profiles

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns `503 temporarily_unavailable` (not billed, `Retry-After` set) — see https://docs.scrapebadger.com/instagram/overview.

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

api_instance = ScrapeBadger::InstagramApi.new
username = 'username_example' # String | 

begin
  # Related profiles
  result = api_instance.instagram_related_profiles(username)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_related_profiles: #{e}"
end
```

#### Using the instagram_related_profiles_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_related_profiles_with_http_info(username)

```ruby
begin
  # Related profiles
  data, status_code, headers = api_instance.instagram_related_profiles_with_http_info(username)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_related_profiles_with_http_info: #{e}"
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


## instagram_search_hashtags

> Object instagram_search_hashtags(query)

Search hashtags

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns `503 temporarily_unavailable` (not billed, `Retry-After` set) — see https://docs.scrapebadger.com/instagram/overview.

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

api_instance = ScrapeBadger::InstagramApi.new
query = 'query_example' # String | 

begin
  # Search hashtags
  result = api_instance.instagram_search_hashtags(query)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_search_hashtags: #{e}"
end
```

#### Using the instagram_search_hashtags_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_search_hashtags_with_http_info(query)

```ruby
begin
  # Search hashtags
  data, status_code, headers = api_instance.instagram_search_hashtags_with_http_info(query)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_search_hashtags_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## instagram_search_users

> Object instagram_search_users(query)

Search users

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns `503 temporarily_unavailable` (not billed, `Retry-After` set) — see https://docs.scrapebadger.com/instagram/overview.

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

api_instance = ScrapeBadger::InstagramApi.new
query = 'query_example' # String | 

begin
  # Search users
  result = api_instance.instagram_search_users(query)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_search_users: #{e}"
end
```

#### Using the instagram_search_users_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_search_users_with_http_info(query)

```ruby
begin
  # Search users
  data, status_code, headers = api_instance.instagram_search_users_with_http_info(query)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_search_users_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## instagram_top_hashtag_posts

> Object instagram_top_hashtag_posts(tag, opts)

Top hashtag posts

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns `503 temporarily_unavailable` (not billed, `Retry-After` set) — see https://docs.scrapebadger.com/instagram/overview.

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

api_instance = ScrapeBadger::InstagramApi.new
tag = 'tag_example' # String | 
opts = {
  amount: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # Top hashtag posts
  result = api_instance.instagram_top_hashtag_posts(tag, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_top_hashtag_posts: #{e}"
end
```

#### Using the instagram_top_hashtag_posts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> instagram_top_hashtag_posts_with_http_info(tag, opts)

```ruby
begin
  # Top hashtag posts
  data, status_code, headers = api_instance.instagram_top_hashtag_posts_with_http_info(tag, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling InstagramApi->instagram_top_hashtag_posts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tag** | **String** |  |  |
| **amount** | **Integer** |  | [optional][default to 20] |
| **cursor** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

