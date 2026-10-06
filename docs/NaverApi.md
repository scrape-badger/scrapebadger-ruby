# ScrapeBadger::NaverApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**naver_naver_blog_search**](NaverApi.md#naver_naver_blog_search) | **GET** /v1/naver/blog | Naver blog search |
| [**naver_naver_datalab_shopping_keyword_insight**](NaverApi.md#naver_naver_datalab_shopping_keyword_insight) | **GET** /v1/naver/shopping/insight | Naver DataLab shopping keyword insight |
| [**naver_naver_news_search**](NaverApi.md#naver_naver_news_search) | **GET** /v1/naver/news | Naver news search |
| [**naver_naver_place_detail**](NaverApi.md#naver_naver_place_detail) | **GET** /v1/naver/place/{place_id} | Naver place detail |
| [**naver_naver_place_local_search**](NaverApi.md#naver_naver_place_local_search) | **GET** /v1/naver/local | Naver Place/Local search |
| [**naver_naver_place_visitor_reviews**](NaverApi.md#naver_naver_place_visitor_reviews) | **GET** /v1/naver/place/{place_id}/reviews | Naver place visitor reviews |
| [**naver_naver_scraper_health_check**](NaverApi.md#naver_naver_scraper_health_check) | **GET** /v1/naver/health | Naver scraper health check |
| [**naver_naver_scraper_health_check_head**](NaverApi.md#naver_naver_scraper_health_check_head) | **HEAD** /v1/naver/health | Naver scraper health check |
| [**naver_naver_shopping_bestseller_rankings**](NaverApi.md#naver_naver_shopping_bestseller_rankings) | **GET** /v1/naver/shopping/bestsellers | Naver Shopping bestseller rankings |
| [**naver_naver_shopping_category_reference**](NaverApi.md#naver_naver_shopping_category_reference) | **GET** /v1/naver/shopping/categories | Naver Shopping category reference |
| [**naver_naver_shopping_trending_keyword_rankings**](NaverApi.md#naver_naver_shopping_trending_keyword_rankings) | **GET** /v1/naver/shopping/keywords | Naver Shopping trending keyword rankings |
| [**naver_naver_web_search**](NaverApi.md#naver_naver_web_search) | **GET** /v1/naver/search | Naver web search |
| [**naver_search_suggestions**](NaverApi.md#naver_search_suggestions) | **GET** /v1/naver/autocomplete | Search suggestions |


## naver_naver_blog_search

> Object naver_naver_blog_search(query, opts)

Naver blog search

Naver blog vertical — post title, blog name and real post URLs.

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

api_instance = ScrapeBadger::NaverApi.new
query = 'query_example' # String | 검색어
opts = {
  page: 56 # Integer | 
}

begin
  # Naver blog search
  result = api_instance.naver_naver_blog_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_blog_search: #{e}"
end
```

#### Using the naver_naver_blog_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> naver_naver_blog_search_with_http_info(query, opts)

```ruby
begin
  # Naver blog search
  data, status_code, headers = api_instance.naver_naver_blog_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_blog_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | 검색어 |  |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## naver_naver_datalab_shopping_keyword_insight

> Object naver_naver_datalab_shopping_keyword_insight(category_id, start_date, end_date, opts)

Naver DataLab shopping keyword insight

DataLab Shopping Insight — top search keywords in a category over a window.

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

api_instance = ScrapeBadger::NaverApi.new
category_id = 'category_id_example' # String | DataLab category id (cid), e.g. 50000000
start_date = 'start_date_example' # String | YYYY-MM-DD
end_date = 'end_date_example' # String | YYYY-MM-DD
opts = {
  time_unit: 'time_unit_example', # String | date | week | month
  count: 56 # Integer | Keywords to return
}

begin
  # Naver DataLab shopping keyword insight
  result = api_instance.naver_naver_datalab_shopping_keyword_insight(category_id, start_date, end_date, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_datalab_shopping_keyword_insight: #{e}"
end
```

#### Using the naver_naver_datalab_shopping_keyword_insight_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> naver_naver_datalab_shopping_keyword_insight_with_http_info(category_id, start_date, end_date, opts)

```ruby
begin
  # Naver DataLab shopping keyword insight
  data, status_code, headers = api_instance.naver_naver_datalab_shopping_keyword_insight_with_http_info(category_id, start_date, end_date, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_datalab_shopping_keyword_insight_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category_id** | **String** | DataLab category id (cid), e.g. 50000000 |  |
| **start_date** | **String** | YYYY-MM-DD |  |
| **end_date** | **String** | YYYY-MM-DD |  |
| **time_unit** | **String** | date | week | month | [optional][default to &#39;date&#39;] |
| **count** | **Integer** | Keywords to return | [optional][default to 20] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## naver_naver_news_search

> Object naver_naver_news_search(query, opts)

Naver news search

Naver news vertical — publisher, age string and real article URLs.

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

api_instance = ScrapeBadger::NaverApi.new
query = 'query_example' # String | 검색어
opts = {
  page: 56 # Integer | 
}

begin
  # Naver news search
  result = api_instance.naver_naver_news_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_news_search: #{e}"
end
```

#### Using the naver_naver_news_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> naver_naver_news_search_with_http_info(query, opts)

```ruby
begin
  # Naver news search
  data, status_code, headers = api_instance.naver_naver_news_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_news_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | 검색어 |  |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## naver_naver_place_detail

> Object naver_naver_place_detail(place_id)

Naver place detail

Naver Place detail by place id.

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

api_instance = ScrapeBadger::NaverApi.new
place_id = 'place_id_example' # String | 

begin
  # Naver place detail
  result = api_instance.naver_naver_place_detail(place_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_place_detail: #{e}"
end
```

#### Using the naver_naver_place_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> naver_naver_place_detail_with_http_info(place_id)

```ruby
begin
  # Naver place detail
  data, status_code, headers = api_instance.naver_naver_place_detail_with_http_info(place_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_place_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **place_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## naver_naver_place_local_search

> Object naver_naver_place_local_search(query)

Naver Place/Local search

Naver Place/Local search — name, category, rating, hours status.

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

api_instance = ScrapeBadger::NaverApi.new
query = 'query_example' # String | Place query, e.g. '성남 카페'

begin
  # Naver Place/Local search
  result = api_instance.naver_naver_place_local_search(query)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_place_local_search: #{e}"
end
```

#### Using the naver_naver_place_local_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> naver_naver_place_local_search_with_http_info(query)

```ruby
begin
  # Naver Place/Local search
  data, status_code, headers = api_instance.naver_naver_place_local_search_with_http_info(query)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_place_local_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Place query, e.g. &#39;성남 카페&#39; |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## naver_naver_place_visitor_reviews

> Object naver_naver_place_visitor_reviews(place_id)

Naver place visitor reviews

Visitor reviews for a Naver place — rating, body, reviewer, voted keywords, photos.

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

api_instance = ScrapeBadger::NaverApi.new
place_id = 'place_id_example' # String | 

begin
  # Naver place visitor reviews
  result = api_instance.naver_naver_place_visitor_reviews(place_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_place_visitor_reviews: #{e}"
end
```

#### Using the naver_naver_place_visitor_reviews_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> naver_naver_place_visitor_reviews_with_http_info(place_id)

```ruby
begin
  # Naver place visitor reviews
  data, status_code, headers = api_instance.naver_naver_place_visitor_reviews_with_http_info(place_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_place_visitor_reviews_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **place_id** | **String** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## naver_naver_scraper_health_check

> Object naver_naver_scraper_health_check

Naver scraper health check

Check health of the Naver scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::NaverApi.new

begin
  # Naver scraper health check
  result = api_instance.naver_naver_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_scraper_health_check: #{e}"
end
```

#### Using the naver_naver_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> naver_naver_scraper_health_check_with_http_info

```ruby
begin
  # Naver scraper health check
  data, status_code, headers = api_instance.naver_naver_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_scraper_health_check_with_http_info: #{e}"
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


## naver_naver_scraper_health_check_head

> Object naver_naver_scraper_health_check_head

Naver scraper health check

Check health of the Naver scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::NaverApi.new

begin
  # Naver scraper health check
  result = api_instance.naver_naver_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_scraper_health_check_head: #{e}"
end
```

#### Using the naver_naver_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> naver_naver_scraper_health_check_head_with_http_info

```ruby
begin
  # Naver scraper health check
  data, status_code, headers = api_instance.naver_naver_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_scraper_health_check_head_with_http_info: #{e}"
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


## naver_naver_shopping_bestseller_rankings

> Object naver_naver_shopping_bestseller_rankings(opts)

Naver Shopping bestseller rankings

Naver Shopping bestseller rankings — ranked products with price, review score, mall.

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

api_instance = ScrapeBadger::NaverApi.new
opts = {
  category_id: 'category_id_example', # String | Naver shopping category id, or ALL
  age_type: 'age_type_example', # String | ALL | MEN_20 | WOMEN_20 | ...
  sort_type: 'sort_type_example', # String | PRODUCT_CLICK | PRODUCT_BUY
  period_type: 'period_type_example' # String | DAILY | WEEKLY
}

begin
  # Naver Shopping bestseller rankings
  result = api_instance.naver_naver_shopping_bestseller_rankings(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_shopping_bestseller_rankings: #{e}"
end
```

#### Using the naver_naver_shopping_bestseller_rankings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> naver_naver_shopping_bestseller_rankings_with_http_info(opts)

```ruby
begin
  # Naver Shopping bestseller rankings
  data, status_code, headers = api_instance.naver_naver_shopping_bestseller_rankings_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_shopping_bestseller_rankings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category_id** | **String** | Naver shopping category id, or ALL | [optional][default to &#39;ALL&#39;] |
| **age_type** | **String** | ALL | MEN_20 | WOMEN_20 | ... | [optional][default to &#39;ALL&#39;] |
| **sort_type** | **String** | PRODUCT_CLICK | PRODUCT_BUY | [optional][default to &#39;PRODUCT_CLICK&#39;] |
| **period_type** | **String** | DAILY | WEEKLY | [optional][default to &#39;DAILY&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## naver_naver_shopping_category_reference

> Object naver_naver_shopping_category_reference

Naver Shopping category reference

Naver Shopping top-level category ids (for bestsellers/keywords/insight). Free.

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

api_instance = ScrapeBadger::NaverApi.new

begin
  # Naver Shopping category reference
  result = api_instance.naver_naver_shopping_category_reference
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_shopping_category_reference: #{e}"
end
```

#### Using the naver_naver_shopping_category_reference_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> naver_naver_shopping_category_reference_with_http_info

```ruby
begin
  # Naver Shopping category reference
  data, status_code, headers = api_instance.naver_naver_shopping_category_reference_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_shopping_category_reference_with_http_info: #{e}"
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


## naver_naver_shopping_trending_keyword_rankings

> Object naver_naver_shopping_trending_keyword_rankings(category_id, opts)

Naver Shopping trending keyword rankings

Trending Naver Shopping keywords for a category (snxbest keyword rankings).

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

api_instance = ScrapeBadger::NaverApi.new
category_id = 'category_id_example' # String | Naver shopping category id (see /shopping/categories)
opts = {
  age_type: 'age_type_example', # String | ALL | MEN_20 | WOMEN_20 | ...
  sort_type: 'sort_type_example', # String | 
  period_type: 'period_type_example' # String | DAILY | WEEKLY
}

begin
  # Naver Shopping trending keyword rankings
  result = api_instance.naver_naver_shopping_trending_keyword_rankings(category_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_shopping_trending_keyword_rankings: #{e}"
end
```

#### Using the naver_naver_shopping_trending_keyword_rankings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> naver_naver_shopping_trending_keyword_rankings_with_http_info(category_id, opts)

```ruby
begin
  # Naver Shopping trending keyword rankings
  data, status_code, headers = api_instance.naver_naver_shopping_trending_keyword_rankings_with_http_info(category_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_shopping_trending_keyword_rankings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category_id** | **String** | Naver shopping category id (see /shopping/categories) |  |
| **age_type** | **String** | ALL | MEN_20 | WOMEN_20 | ... | [optional][default to &#39;ALL&#39;] |
| **sort_type** | **String** |  | [optional][default to &#39;KEYWORD_POPULAR&#39;] |
| **period_type** | **String** | DAILY | WEEKLY | [optional][default to &#39;WEEKLY&#39;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## naver_naver_web_search

> Object naver_naver_web_search(query, opts)

Naver web search

Naver integrated SERP — organic results plus the inline Place pack.

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

api_instance = ScrapeBadger::NaverApi.new
query = 'query_example' # String | 검색어, e.g. '성남 카페'
opts = {
  page: 56 # Integer | Result page
}

begin
  # Naver web search
  result = api_instance.naver_naver_web_search(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_web_search: #{e}"
end
```

#### Using the naver_naver_web_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> naver_naver_web_search_with_http_info(query, opts)

```ruby
begin
  # Naver web search
  data, status_code, headers = api_instance.naver_naver_web_search_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_naver_web_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | 검색어, e.g. &#39;성남 카페&#39; |  |
| **page** | **Integer** | Result page | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## naver_search_suggestions

> Object naver_search_suggestions(query)

Search suggestions

Naver search-box suggestions.

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

api_instance = ScrapeBadger::NaverApi.new
query = 'query_example' # String | Partial search term

begin
  # Search suggestions
  result = api_instance.naver_search_suggestions(query)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_search_suggestions: #{e}"
end
```

#### Using the naver_search_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> naver_search_suggestions_with_http_info(query)

```ruby
begin
  # Search suggestions
  data, status_code, headers = api_instance.naver_search_suggestions_with_http_info(query)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling NaverApi->naver_search_suggestions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Partial search term |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

