# ScrapeBadger::AirbnbApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**airbnb_airbnb_scraper_health_check**](AirbnbApi.md#airbnb_airbnb_scraper_health_check) | **GET** /v1/airbnb/health | Airbnb scraper health check |
| [**airbnb_airbnb_scraper_health_check_head**](AirbnbApi.md#airbnb_airbnb_scraper_health_check_head) | **HEAD** /v1/airbnb/health | Airbnb scraper health check |
| [**airbnb_get_availability_calendar**](AirbnbApi.md#airbnb_get_availability_calendar) | **GET** /v1/airbnb/listings/{room_id}/calendar | Get availability calendar |
| [**airbnb_get_experience_detail**](AirbnbApi.md#airbnb_get_experience_detail) | **GET** /v1/airbnb/experiences/{experience_id} | Get experience detail |
| [**airbnb_get_listing_detail**](AirbnbApi.md#airbnb_get_listing_detail) | **GET** /v1/airbnb/listings/{room_id} | Get listing detail |
| [**airbnb_get_listing_reviews**](AirbnbApi.md#airbnb_get_listing_reviews) | **GET** /v1/airbnb/listings/{room_id}/reviews | Get listing reviews |
| [**airbnb_search_experiences**](AirbnbApi.md#airbnb_search_experiences) | **GET** /v1/airbnb/experiences | Search experiences |
| [**airbnb_search_stays**](AirbnbApi.md#airbnb_search_stays) | **GET** /v1/airbnb/search | Search stays |


## airbnb_airbnb_scraper_health_check

> Object airbnb_airbnb_scraper_health_check

Airbnb scraper health check

Check health of the Airbnb scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::AirbnbApi.new

begin
  # Airbnb scraper health check
  result = api_instance.airbnb_airbnb_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AirbnbApi->airbnb_airbnb_scraper_health_check: #{e}"
end
```

#### Using the airbnb_airbnb_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> airbnb_airbnb_scraper_health_check_with_http_info

```ruby
begin
  # Airbnb scraper health check
  data, status_code, headers = api_instance.airbnb_airbnb_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AirbnbApi->airbnb_airbnb_scraper_health_check_with_http_info: #{e}"
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


## airbnb_airbnb_scraper_health_check_head

> Object airbnb_airbnb_scraper_health_check_head

Airbnb scraper health check

Check health of the Airbnb scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::AirbnbApi.new

begin
  # Airbnb scraper health check
  result = api_instance.airbnb_airbnb_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AirbnbApi->airbnb_airbnb_scraper_health_check_head: #{e}"
end
```

#### Using the airbnb_airbnb_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> airbnb_airbnb_scraper_health_check_head_with_http_info

```ruby
begin
  # Airbnb scraper health check
  data, status_code, headers = api_instance.airbnb_airbnb_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AirbnbApi->airbnb_airbnb_scraper_health_check_head_with_http_info: #{e}"
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


## airbnb_get_availability_calendar

> Object airbnb_get_availability_calendar(room_id, opts)

Get availability calendar

Day-by-day availability for up to 12 months: bookable, check-in/out windows and min/max nights per date.

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

api_instance = ScrapeBadger::AirbnbApi.new
room_id = 'room_id_example' # String | 
opts = {
  month: 56, # Integer | Start month (1-12)
  year: 56, # Integer | Start year
  months: 56, # Integer | Number of months (max 12)
  currency: 'currency_example', # String | 
  locale: 'locale_example' # String | 
}

begin
  # Get availability calendar
  result = api_instance.airbnb_get_availability_calendar(room_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AirbnbApi->airbnb_get_availability_calendar: #{e}"
end
```

#### Using the airbnb_get_availability_calendar_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> airbnb_get_availability_calendar_with_http_info(room_id, opts)

```ruby
begin
  # Get availability calendar
  data, status_code, headers = api_instance.airbnb_get_availability_calendar_with_http_info(room_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AirbnbApi->airbnb_get_availability_calendar_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **room_id** | **String** |  |  |
| **month** | **Integer** | Start month (1-12) | [optional][default to 1] |
| **year** | **Integer** | Start year | [optional][default to 2026] |
| **months** | **Integer** | Number of months (max 12) | [optional][default to 12] |
| **currency** | **String** |  | [optional] |
| **locale** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## airbnb_get_experience_detail

> Object airbnb_get_experience_detail(experience_id, opts)

Get experience detail

Full detail for one experience: description, rating, host, location and photos.

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

api_instance = ScrapeBadger::AirbnbApi.new
experience_id = 'experience_id_example' # String | 
opts = {
  adults: 56, # Integer | 
  children: 56, # Integer | 
  infants: 56, # Integer | 
  currency: 'currency_example', # String | 
  locale: 'locale_example' # String | 
}

begin
  # Get experience detail
  result = api_instance.airbnb_get_experience_detail(experience_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AirbnbApi->airbnb_get_experience_detail: #{e}"
end
```

#### Using the airbnb_get_experience_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> airbnb_get_experience_detail_with_http_info(experience_id, opts)

```ruby
begin
  # Get experience detail
  data, status_code, headers = api_instance.airbnb_get_experience_detail_with_http_info(experience_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AirbnbApi->airbnb_get_experience_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **experience_id** | **String** |  |  |
| **adults** | **Integer** |  | [optional][default to 1] |
| **children** | **Integer** |  | [optional][default to 0] |
| **infants** | **Integer** |  | [optional][default to 0] |
| **currency** | **String** |  | [optional] |
| **locale** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## airbnb_get_listing_detail

> Object airbnb_get_listing_detail(room_id, opts)

Get listing detail

Full detail for one listing: amenities, house rules, host, ratings, coordinates and photos.

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

api_instance = ScrapeBadger::AirbnbApi.new
room_id = 'room_id_example' # String | 
opts = {
  adults: 56, # Integer | 
  currency: 'currency_example', # String | 
  locale: 'locale_example' # String | 
}

begin
  # Get listing detail
  result = api_instance.airbnb_get_listing_detail(room_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AirbnbApi->airbnb_get_listing_detail: #{e}"
end
```

#### Using the airbnb_get_listing_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> airbnb_get_listing_detail_with_http_info(room_id, opts)

```ruby
begin
  # Get listing detail
  data, status_code, headers = api_instance.airbnb_get_listing_detail_with_http_info(room_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AirbnbApi->airbnb_get_listing_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **room_id** | **String** |  |  |
| **adults** | **Integer** |  | [optional][default to 1] |
| **currency** | **String** |  | [optional] |
| **locale** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## airbnb_get_listing_reviews

> Object airbnb_get_listing_reviews(room_id, opts)

Get listing reviews

Paginated guest reviews with reviewer, rating, date, text and host response.

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

api_instance = ScrapeBadger::AirbnbApi.new
room_id = 'room_id_example' # String | 
opts = {
  limit: 56, # Integer | 
  offset: 56, # Integer | 
  sort: 'sort_example', # String | MOST_RECENT | RATING_DESC | RATING_ASC
  currency: 'currency_example', # String | 
  locale: 'locale_example' # String | 
}

begin
  # Get listing reviews
  result = api_instance.airbnb_get_listing_reviews(room_id, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AirbnbApi->airbnb_get_listing_reviews: #{e}"
end
```

#### Using the airbnb_get_listing_reviews_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> airbnb_get_listing_reviews_with_http_info(room_id, opts)

```ruby
begin
  # Get listing reviews
  data, status_code, headers = api_instance.airbnb_get_listing_reviews_with_http_info(room_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AirbnbApi->airbnb_get_listing_reviews_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **room_id** | **String** |  |  |
| **limit** | **Integer** |  | [optional][default to 24] |
| **offset** | **Integer** |  | [optional][default to 0] |
| **sort** | **String** | MOST_RECENT | RATING_DESC | RATING_ASC | [optional][default to &#39;MOST_RECENT&#39;] |
| **currency** | **String** |  | [optional] |
| **locale** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## airbnb_search_experiences

> Object airbnb_search_experiences(location, opts)

Search experiences

Search Airbnb Experiences by location.

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

api_instance = ScrapeBadger::AirbnbApi.new
location = 'location_example' # String | Free-text place, e.g. 'Rome, Italy'
opts = {
  cursor: 'cursor_example', # String | next_page_cursor from a prior response
  currency: 'currency_example', # String | 
  locale: 'locale_example' # String | 
}

begin
  # Search experiences
  result = api_instance.airbnb_search_experiences(location, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AirbnbApi->airbnb_search_experiences: #{e}"
end
```

#### Using the airbnb_search_experiences_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> airbnb_search_experiences_with_http_info(location, opts)

```ruby
begin
  # Search experiences
  data, status_code, headers = api_instance.airbnb_search_experiences_with_http_info(location, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AirbnbApi->airbnb_search_experiences_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **location** | **String** | Free-text place, e.g. &#39;Rome, Italy&#39; |  |
| **cursor** | **String** | next_page_cursor from a prior response | [optional] |
| **currency** | **String** |  | [optional] |
| **locale** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## airbnb_search_stays

> Object airbnb_search_stays(opts)

Search stays

Search Airbnb stays by place name and/or map bounding box, with dates, guests, price and property filters. Paginate with the `cursor`.

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

api_instance = ScrapeBadger::AirbnbApi.new
opts = {
  location: 'location_example', # String | Free-text place, e.g. 'Paris, France'
  ne_lat: 8.14, # Float | Map bounding-box NE latitude
  ne_lng: 8.14, # Float | Map bounding-box NE longitude
  sw_lat: 8.14, # Float | Map bounding-box SW latitude
  sw_lng: 8.14, # Float | Map bounding-box SW longitude
  check_in: 'check_in_example', # String | Check-in date YYYY-MM-DD
  check_out: 'check_out_example', # String | Check-out date YYYY-MM-DD
  adults: 56, # Integer | 
  children: 56, # Integer | 
  infants: 56, # Integer | 
  pets: 56, # Integer | 
  price_min: 56, # Integer | 
  price_max: 56, # Integer | 
  min_bedrooms: 56, # Integer | 
  min_beds: 56, # Integer | 
  min_bathrooms: 56, # Integer | 
  room_type: 'room_type_example', # String | e.g. 'Entire home/apt', 'Private room'
  cursor: 'cursor_example', # String | next_page_cursor from a prior response
  limit: 56, # Integer | 
  currency: 'currency_example', # String | ISO currency, e.g. USD, EUR
  locale: 'locale_example' # String | Locale, e.g. en, fr
}

begin
  # Search stays
  result = api_instance.airbnb_search_stays(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AirbnbApi->airbnb_search_stays: #{e}"
end
```

#### Using the airbnb_search_stays_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> airbnb_search_stays_with_http_info(opts)

```ruby
begin
  # Search stays
  data, status_code, headers = api_instance.airbnb_search_stays_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling AirbnbApi->airbnb_search_stays_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **location** | **String** | Free-text place, e.g. &#39;Paris, France&#39; | [optional] |
| **ne_lat** | **Float** | Map bounding-box NE latitude | [optional] |
| **ne_lng** | **Float** | Map bounding-box NE longitude | [optional] |
| **sw_lat** | **Float** | Map bounding-box SW latitude | [optional] |
| **sw_lng** | **Float** | Map bounding-box SW longitude | [optional] |
| **check_in** | **String** | Check-in date YYYY-MM-DD | [optional] |
| **check_out** | **String** | Check-out date YYYY-MM-DD | [optional] |
| **adults** | **Integer** |  | [optional][default to 1] |
| **children** | **Integer** |  | [optional][default to 0] |
| **infants** | **Integer** |  | [optional][default to 0] |
| **pets** | **Integer** |  | [optional][default to 0] |
| **price_min** | **Integer** |  | [optional] |
| **price_max** | **Integer** |  | [optional] |
| **min_bedrooms** | **Integer** |  | [optional] |
| **min_beds** | **Integer** |  | [optional] |
| **min_bathrooms** | **Integer** |  | [optional] |
| **room_type** | **String** | e.g. &#39;Entire home/apt&#39;, &#39;Private room&#39; | [optional] |
| **cursor** | **String** | next_page_cursor from a prior response | [optional] |
| **limit** | **Integer** |  | [optional][default to 18] |
| **currency** | **String** | ISO currency, e.g. USD, EUR | [optional] |
| **locale** | **String** | Locale, e.g. en, fr | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

