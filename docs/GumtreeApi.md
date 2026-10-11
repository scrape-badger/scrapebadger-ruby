# ScrapeBadger::GumtreeApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**gumtree_get_listing**](GumtreeApi.md#gumtree_get_listing) | **GET** /v1/gumtree/listings/{listing_id} | Get listing |
| [**gumtree_get_search_filters**](GumtreeApi.md#gumtree_get_search_filters) | **GET** /v1/gumtree/search/filters | Get search filters |
| [**gumtree_get_seller_listings**](GumtreeApi.md#gumtree_get_seller_listings) | **GET** /v1/gumtree/listings/{listing_id}/seller-listings | Get seller listings |
| [**gumtree_gumtree_scraper_health_check**](GumtreeApi.md#gumtree_gumtree_scraper_health_check) | **GET** /v1/gumtree/health | Gumtree scraper health check |
| [**gumtree_gumtree_scraper_health_check_head**](GumtreeApi.md#gumtree_gumtree_scraper_health_check_head) | **HEAD** /v1/gumtree/health | Gumtree scraper health check |
| [**gumtree_list_categories**](GumtreeApi.md#gumtree_list_categories) | **GET** /v1/gumtree/categories | List categories |
| [**gumtree_list_locations**](GumtreeApi.md#gumtree_list_locations) | **GET** /v1/gumtree/locations | List locations |
| [**gumtree_location_suggestions**](GumtreeApi.md#gumtree_location_suggestions) | **GET** /v1/gumtree/locations/autocomplete | Location suggestions |
| [**gumtree_search_listings**](GumtreeApi.md#gumtree_search_listings) | **GET** /v1/gumtree/search | Search listings |
| [**gumtree_search_suggestions**](GumtreeApi.md#gumtree_search_suggestions) | **GET** /v1/gumtree/autocomplete | Search suggestions |


## gumtree_get_listing

> Object gumtree_get_listing(listing_id)

Get listing

Full listing — description, attributes, images, seller, similar listings.

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

api_instance = ScrapeBadger::GumtreeApi.new
listing_id = 'listing_id_example' # String | Gumtree listing id — the number at the end of a gumtree.com/p/... URL

begin
  # Get listing
  result = api_instance.gumtree_get_listing(listing_id)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_get_listing: #{e}"
end
```

#### Using the gumtree_get_listing_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_get_listing_with_http_info(listing_id)

```ruby
begin
  # Get listing
  data, status_code, headers = api_instance.gumtree_get_listing_with_http_info(listing_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_get_listing_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **listing_id** | **String** | Gumtree listing id — the number at the end of a gumtree.com/p/... URL |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## gumtree_get_search_filters

> Object gumtree_get_search_filters(opts)

Get search filters

Filters, sort orders and radius options for a category, with live counts.

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

api_instance = ScrapeBadger::GumtreeApi.new
opts = {
  category: 'category_example', # String | Category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs'. Default 'all'.
  location: 'location_example', # String | Location slug ('london'), town name or UK postcode ('SW1A 1AA'). Default 'uk'.
  query: 'query_example' # String | 
}

begin
  # Get search filters
  result = api_instance.gumtree_get_search_filters(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_get_search_filters: #{e}"
end
```

#### Using the gumtree_get_search_filters_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_get_search_filters_with_http_info(opts)

```ruby
begin
  # Get search filters
  data, status_code, headers = api_instance.gumtree_get_search_filters_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_get_search_filters_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **category** | **String** | Category slug, e.g. &#39;cars&#39;, &#39;for-sale&#39;, &#39;property-to-rent&#39;, &#39;jobs&#39;. Default &#39;all&#39;. | [optional][default to &#39;all&#39;] |
| **location** | **String** | Location slug (&#39;london&#39;), town name or UK postcode (&#39;SW1A 1AA&#39;). Default &#39;uk&#39;. | [optional][default to &#39;uk&#39;] |
| **query** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## gumtree_get_seller_listings

> Object gumtree_get_seller_listings(listing_id, opts)

Get seller listings

Every live listing by the seller of the given listing.

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

api_instance = ScrapeBadger::GumtreeApi.new
listing_id = 'listing_id_example' # String | Gumtree listing id — the number at the end of a gumtree.com/p/... URL
opts = {
  page: 56 # Integer | 
}

begin
  # Get seller listings
  result = api_instance.gumtree_get_seller_listings(listing_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_get_seller_listings: #{e}"
end
```

#### Using the gumtree_get_seller_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_get_seller_listings_with_http_info(listing_id, opts)

```ruby
begin
  # Get seller listings
  data, status_code, headers = api_instance.gumtree_get_seller_listings_with_http_info(listing_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_get_seller_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **listing_id** | **String** | Gumtree listing id — the number at the end of a gumtree.com/p/... URL |  |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## gumtree_gumtree_scraper_health_check

> Object gumtree_gumtree_scraper_health_check

Gumtree scraper health check

Check health of the Gumtree scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::GumtreeApi.new

begin
  # Gumtree scraper health check
  result = api_instance.gumtree_gumtree_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_gumtree_scraper_health_check: #{e}"
end
```

#### Using the gumtree_gumtree_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_gumtree_scraper_health_check_with_http_info

```ruby
begin
  # Gumtree scraper health check
  data, status_code, headers = api_instance.gumtree_gumtree_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_gumtree_scraper_health_check_with_http_info: #{e}"
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


## gumtree_gumtree_scraper_health_check_head

> Object gumtree_gumtree_scraper_health_check_head

Gumtree scraper health check

Check health of the Gumtree scraper service (accepts HEAD for UptimeRobot).

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

api_instance = ScrapeBadger::GumtreeApi.new

begin
  # Gumtree scraper health check
  result = api_instance.gumtree_gumtree_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_gumtree_scraper_health_check_head: #{e}"
end
```

#### Using the gumtree_gumtree_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_gumtree_scraper_health_check_head_with_http_info

```ruby
begin
  # Gumtree scraper health check
  data, status_code, headers = api_instance.gumtree_gumtree_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_gumtree_scraper_health_check_head_with_http_info: #{e}"
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


## gumtree_list_categories

> Object gumtree_list_categories(opts)

List categories

Browse Gumtree's category tree. A node's `slug` is the `/search` category.

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

api_instance = ScrapeBadger::GumtreeApi.new
opts = {
  parent_id: 56 # Integer | Parent category id (default: all)
}

begin
  # List categories
  result = api_instance.gumtree_list_categories(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_list_categories: #{e}"
end
```

#### Using the gumtree_list_categories_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_list_categories_with_http_info(opts)

```ruby
begin
  # List categories
  data, status_code, headers = api_instance.gumtree_list_categories_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_list_categories_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **parent_id** | **Integer** | Parent category id (default: all) | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## gumtree_list_locations

> Object gumtree_list_locations(opts)

List locations

Browse Gumtree's location tree.

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

api_instance = ScrapeBadger::GumtreeApi.new
opts = {
  parent_id: 56 # Integer | Parent location id (default: UK)
}

begin
  # List locations
  result = api_instance.gumtree_list_locations(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_list_locations: #{e}"
end
```

#### Using the gumtree_list_locations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_list_locations_with_http_info(opts)

```ruby
begin
  # List locations
  data, status_code, headers = api_instance.gumtree_list_locations_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_list_locations_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **parent_id** | **Integer** | Parent location id (default: UK) | [optional][default to 10000392] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## gumtree_location_suggestions

> Object gumtree_location_suggestions(query)

Location suggestions

Resolve a place name or postcode to Gumtree locations with coordinates.

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

api_instance = ScrapeBadger::GumtreeApi.new
query = 'query_example' # String | Town or postcode prefix, e.g. 'manch'

begin
  # Location suggestions
  result = api_instance.gumtree_location_suggestions(query)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_location_suggestions: #{e}"
end
```

#### Using the gumtree_location_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_location_suggestions_with_http_info(query)

```ruby
begin
  # Location suggestions
  data, status_code, headers = api_instance.gumtree_location_suggestions_with_http_info(query)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_location_suggestions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Town or postcode prefix, e.g. &#39;manch&#39; |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## gumtree_search_listings

> Object gumtree_search_listings(opts)

Search listings

Search gumtree.com listings. ~25-30 per page, up to 50 pages.

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

api_instance = ScrapeBadger::GumtreeApi.new
opts = {
  query: 'query_example', # String | Search keywords, e.g. 'mountain bike'
  category: 'category_example', # String | Category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs'. Default 'all'.
  location: 'location_example', # String | Location slug ('london'), town name or UK postcode ('SW1A 1AA'). Default 'uk'.
  distance: 8.14, # Float | Radius in miles
  min_price: 56, # Integer | GBP; needs a category
  max_price: 56, # Integer | GBP; needs a category
  sort: 'relevance', # String | 
  seller_type: 'private', # String | 
  urgent_only: true, # Boolean | 
  with_photos: true, # Boolean | 
  filters: 'filters_example', # String | Category filters as key:value pairs, e.g. 'vehicle_make:bmw,vehicle_fuel_type:petrol'
  page: 56 # Integer | 
}

begin
  # Search listings
  result = api_instance.gumtree_search_listings(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_search_listings: #{e}"
end
```

#### Using the gumtree_search_listings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_search_listings_with_http_info(opts)

```ruby
begin
  # Search listings
  data, status_code, headers = api_instance.gumtree_search_listings_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_search_listings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Search keywords, e.g. &#39;mountain bike&#39; | [optional] |
| **category** | **String** | Category slug, e.g. &#39;cars&#39;, &#39;for-sale&#39;, &#39;property-to-rent&#39;, &#39;jobs&#39;. Default &#39;all&#39;. | [optional][default to &#39;all&#39;] |
| **location** | **String** | Location slug (&#39;london&#39;), town name or UK postcode (&#39;SW1A 1AA&#39;). Default &#39;uk&#39;. | [optional][default to &#39;uk&#39;] |
| **distance** | **Float** | Radius in miles | [optional] |
| **min_price** | **Integer** | GBP; needs a category | [optional] |
| **max_price** | **Integer** | GBP; needs a category | [optional] |
| **sort** | **String** |  | [optional] |
| **seller_type** | **String** |  | [optional] |
| **urgent_only** | **Boolean** |  | [optional][default to false] |
| **with_photos** | **Boolean** |  | [optional][default to false] |
| **filters** | **String** | Category filters as key:value pairs, e.g. &#39;vehicle_make:bmw,vehicle_fuel_type:petrol&#39; | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## gumtree_search_suggestions

> Object gumtree_search_suggestions(query)

Search suggestions

Gumtree search-box keyword suggestions with their categories.

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

api_instance = ScrapeBadger::GumtreeApi.new
query = 'query_example' # String | Partial search term, e.g. 'iph'

begin
  # Search suggestions
  result = api_instance.gumtree_search_suggestions(query)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_search_suggestions: #{e}"
end
```

#### Using the gumtree_search_suggestions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> gumtree_search_suggestions_with_http_info(query)

```ruby
begin
  # Search suggestions
  data, status_code, headers = api_instance.gumtree_search_suggestions_with_http_info(query)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling GumtreeApi->gumtree_search_suggestions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Partial search term, e.g. &#39;iph&#39; |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

