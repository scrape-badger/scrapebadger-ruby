# ScrapeBadger::BookingApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**booking_booking_scraper_health_check**](BookingApi.md#booking_booking_scraper_health_check) | **GET** /v1/booking/health | Booking scraper health check |
| [**booking_booking_scraper_health_check_head**](BookingApi.md#booking_booking_scraper_health_check_head) | **HEAD** /v1/booking/health | Booking scraper health check |
| [**booking_get_property_detail**](BookingApi.md#booking_get_property_detail) | **GET** /v1/booking/properties/{country_code}/{slug} | Get property detail |
| [**booking_get_property_reviews**](BookingApi.md#booking_get_property_reviews) | **GET** /v1/booking/properties/{country_code}/{slug}/reviews | Get property reviews |
| [**booking_get_room_types_and_live_rates**](BookingApi.md#booking_get_room_types_and_live_rates) | **GET** /v1/booking/properties/{country_code}/{slug}/rooms | Get room types and live rates |
| [**booking_search_destinations**](BookingApi.md#booking_search_destinations) | **GET** /v1/booking/destinations | Search destinations |
| [**booking_search_properties**](BookingApi.md#booking_search_properties) | **GET** /v1/booking/search | Search properties |


## booking_booking_scraper_health_check

> Object booking_booking_scraper_health_check

Booking scraper health check

Check health of the Booking scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::BookingApi.new

begin
  # Booking scraper health check
  result = api_instance.booking_booking_scraper_health_check
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BookingApi->booking_booking_scraper_health_check: #{e}"
end
```

#### Using the booking_booking_scraper_health_check_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> booking_booking_scraper_health_check_with_http_info

```ruby
begin
  # Booking scraper health check
  data, status_code, headers = api_instance.booking_booking_scraper_health_check_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BookingApi->booking_booking_scraper_health_check_with_http_info: #{e}"
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


## booking_booking_scraper_health_check_head

> Object booking_booking_scraper_health_check_head

Booking scraper health check

Check health of the Booking scraper service (accepts HEAD).

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

api_instance = ScrapeBadger::BookingApi.new

begin
  # Booking scraper health check
  result = api_instance.booking_booking_scraper_health_check_head
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BookingApi->booking_booking_scraper_health_check_head: #{e}"
end
```

#### Using the booking_booking_scraper_health_check_head_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> booking_booking_scraper_health_check_head_with_http_info

```ruby
begin
  # Booking scraper health check
  data, status_code, headers = api_instance.booking_booking_scraper_health_check_head_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BookingApi->booking_booking_scraper_health_check_head_with_http_info: #{e}"
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


## booking_get_property_detail

> Object booking_get_property_detail(country_code, slug, opts)

Get property detail

Full detail for one property: description, address and coordinates, star rating, review score with per-category breakdown, facilities, house rules, room types with occupancy and beds, photos and guest Q&A.

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

api_instance = ScrapeBadger::BookingApi.new
country_code = 'country_code_example' # String | Two-letter country code, e.g. 'it'
slug = 'slug_example' # String | Booking page name, e.g. 'hotel-artemide'
opts = {
  photos: 56, # Integer | Gallery photos to return
  questions: 56, # Integer | Guest Q&A pairs to return
  language: 'language_example' # String | Locale, e.g. en-us, fr
}

begin
  # Get property detail
  result = api_instance.booking_get_property_detail(country_code, slug, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BookingApi->booking_get_property_detail: #{e}"
end
```

#### Using the booking_get_property_detail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> booking_get_property_detail_with_http_info(country_code, slug, opts)

```ruby
begin
  # Get property detail
  data, status_code, headers = api_instance.booking_get_property_detail_with_http_info(country_code, slug, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BookingApi->booking_get_property_detail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **country_code** | **String** | Two-letter country code, e.g. &#39;it&#39; |  |
| **slug** | **String** | Booking page name, e.g. &#39;hotel-artemide&#39; |  |
| **photos** | **Integer** | Gallery photos to return | [optional][default to 40] |
| **questions** | **Integer** | Guest Q&amp;A pairs to return | [optional][default to 10] |
| **language** | **String** | Locale, e.g. en-us, fr | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## booking_get_property_reviews

> Object booking_get_property_reviews(country_code, slug, opts)

Get property reviews

Paginated guest reviews with score, positive and negative text, stay dates, room type, guest country and type, photos and the partner's reply.

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

api_instance = ScrapeBadger::BookingApi.new
country_code = 'country_code_example' # String | Two-letter country code, e.g. 'it'
slug = 'slug_example' # String | Booking page name, e.g. 'hotel-artemide'
opts = {
  limit: 56, # Integer | 
  offset: 56, # Integer | 
  sort: 'sort_example', # String | MOST_RELEVANT | NEWEST_FIRST | OLDEST_FIRST | SCORE_DESC | SCORE_ASC
  review_language: 'review_language_example', # String | Only reviews written in this language, e.g. 'fr'
  guest_type: 'guest_type_example', # String | FAMILIES | COUPLES | GROUP_OF_FRIENDS | SOLO_TRAVELLERS | BUSINESS_TRAVELLERS
  language: 'language_example' # String | Locale for labels, e.g. en-us
}

begin
  # Get property reviews
  result = api_instance.booking_get_property_reviews(country_code, slug, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BookingApi->booking_get_property_reviews: #{e}"
end
```

#### Using the booking_get_property_reviews_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> booking_get_property_reviews_with_http_info(country_code, slug, opts)

```ruby
begin
  # Get property reviews
  data, status_code, headers = api_instance.booking_get_property_reviews_with_http_info(country_code, slug, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BookingApi->booking_get_property_reviews_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **country_code** | **String** | Two-letter country code, e.g. &#39;it&#39; |  |
| **slug** | **String** | Booking page name, e.g. &#39;hotel-artemide&#39; |  |
| **limit** | **Integer** |  | [optional][default to 25] |
| **offset** | **Integer** |  | [optional][default to 0] |
| **sort** | **String** | MOST_RELEVANT | NEWEST_FIRST | OLDEST_FIRST | SCORE_DESC | SCORE_ASC | [optional][default to &#39;MOST_RELEVANT&#39;] |
| **review_language** | **String** | Only reviews written in this language, e.g. &#39;fr&#39; | [optional] |
| **guest_type** | **String** | FAMILIES | COUPLES | GROUP_OF_FRIENDS | SOLO_TRAVELLERS | BUSINESS_TRAVELLERS | [optional] |
| **language** | **String** | Locale for labels, e.g. en-us | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## booking_get_room_types_and_live_rates

> Object booking_get_room_types_and_live_rates(country_code, slug, checkin, checkout, opts)

Get room types and live rates

Every room type at one property with every rate bookable on it for the given dates — price, price before discount, price per night, discounts and badges — plus per-room facilities, bed layouts, occupancy and photos. /search returns only the cheapest rate per property; this returns the whole table.

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

api_instance = ScrapeBadger::BookingApi.new
country_code = 'country_code_example' # String | Two-letter country code, e.g. 'it'
slug = 'slug_example' # String | Booking page name, e.g. 'hotel-artemide'
checkin = 'checkin_example' # String | Check-in date YYYY-MM-DD
checkout = 'checkout_example' # String | Check-out date YYYY-MM-DD
opts = {
  adults: 56, # Integer | 
  children: 'children_example', # String | Comma-separated children ages, e.g. '4,9'
  rooms: 56, # Integer | 
  currency: 'currency_example', # String | ISO currency, e.g. EUR, USD, GBP
  language: 'language_example' # String | Locale, e.g. en-us, fr, de
}

begin
  # Get room types and live rates
  result = api_instance.booking_get_room_types_and_live_rates(country_code, slug, checkin, checkout, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BookingApi->booking_get_room_types_and_live_rates: #{e}"
end
```

#### Using the booking_get_room_types_and_live_rates_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> booking_get_room_types_and_live_rates_with_http_info(country_code, slug, checkin, checkout, opts)

```ruby
begin
  # Get room types and live rates
  data, status_code, headers = api_instance.booking_get_room_types_and_live_rates_with_http_info(country_code, slug, checkin, checkout, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BookingApi->booking_get_room_types_and_live_rates_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **country_code** | **String** | Two-letter country code, e.g. &#39;it&#39; |  |
| **slug** | **String** | Booking page name, e.g. &#39;hotel-artemide&#39; |  |
| **checkin** | **String** | Check-in date YYYY-MM-DD |  |
| **checkout** | **String** | Check-out date YYYY-MM-DD |  |
| **adults** | **Integer** |  | [optional][default to 2] |
| **children** | **String** | Comma-separated children ages, e.g. &#39;4,9&#39; | [optional] |
| **rooms** | **Integer** |  | [optional][default to 1] |
| **currency** | **String** | ISO currency, e.g. EUR, USD, GBP | [optional] |
| **language** | **String** | Locale, e.g. en-us, fr, de | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## booking_search_destinations

> Object booking_search_destinations(query, opts)

Search destinations

Resolve a place name to Booking's `dest_id`/`dest_type`, with coordinates and country — feed the pair back into /search for an exact match.

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

api_instance = ScrapeBadger::BookingApi.new
query = 'query_example' # String | Free-text place, e.g. 'amsterd'
opts = {
  limit: 56, # Integer | 
  language: 'language_example' # String | Locale, e.g. en-us, fr
}

begin
  # Search destinations
  result = api_instance.booking_search_destinations(query, opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BookingApi->booking_search_destinations: #{e}"
end
```

#### Using the booking_search_destinations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> booking_search_destinations_with_http_info(query, opts)

```ruby
begin
  # Search destinations
  data, status_code, headers = api_instance.booking_search_destinations_with_http_info(query, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BookingApi->booking_search_destinations_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Free-text place, e.g. &#39;amsterd&#39; |  |
| **limit** | **Integer** |  | [optional][default to 8] |
| **language** | **String** | Locale, e.g. en-us, fr | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## booking_search_properties

> Object booking_search_properties(opts)

Search properties

Search Booking.com properties by destination, with dates, occupancy, sorting and filters. Returns prices, review scores, coordinates, room configuration and photos. Paginate with `offset`.

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

api_instance = ScrapeBadger::BookingApi.new
opts = {
  location: 'location_example', # String | Free-text destination, e.g. 'Rome'
  dest_id: 56, # Integer | Exact destination id (ufi) from /destinations
  dest_type: 'dest_type_example', # String | Destination type, e.g. CITY
  checkin: 'checkin_example', # String | Check-in date YYYY-MM-DD
  checkout: 'checkout_example', # String | Check-out date YYYY-MM-DD
  adults: 56, # Integer | 
  children: 'children_example', # String | Comma-separated children ages, e.g. '4,9'
  rooms: 56, # Integer | 
  offset: 56, # Integer | Result offset for pagination
  limit: 56, # Integer | 
  sort: 'sort_example', # String | popularity | price | class_descending | class_ascending | distance_from_search | bayesian_review_score | review_score_and_price | upsort_bh
  filters: 'filters_example', # String | Semicolon-separated Booking filter ids, e.g. 'class=4'
  currency: 'currency_example', # String | ISO currency, e.g. EUR, USD, GBP
  language: 'language_example' # String | Locale, e.g. en-us, fr, de, es
}

begin
  # Search properties
  result = api_instance.booking_search_properties(opts)
  p result
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BookingApi->booking_search_properties: #{e}"
end
```

#### Using the booking_search_properties_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> booking_search_properties_with_http_info(opts)

```ruby
begin
  # Search properties
  data, status_code, headers = api_instance.booking_search_properties_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ScrapeBadger::ApiError => e
  puts "Error when calling BookingApi->booking_search_properties_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **location** | **String** | Free-text destination, e.g. &#39;Rome&#39; | [optional] |
| **dest_id** | **Integer** | Exact destination id (ufi) from /destinations | [optional] |
| **dest_type** | **String** | Destination type, e.g. CITY | [optional][default to &#39;NO_DEST_TYPE&#39;] |
| **checkin** | **String** | Check-in date YYYY-MM-DD | [optional] |
| **checkout** | **String** | Check-out date YYYY-MM-DD | [optional] |
| **adults** | **Integer** |  | [optional][default to 2] |
| **children** | **String** | Comma-separated children ages, e.g. &#39;4,9&#39; | [optional] |
| **rooms** | **Integer** |  | [optional][default to 1] |
| **offset** | **Integer** | Result offset for pagination | [optional][default to 0] |
| **limit** | **Integer** |  | [optional][default to 25] |
| **sort** | **String** | popularity | price | class_descending | class_ascending | distance_from_search | bayesian_review_score | review_score_and_price | upsort_bh | [optional] |
| **filters** | **String** | Semicolon-separated Booking filter ids, e.g. &#39;class&#x3D;4&#39; | [optional] |
| **currency** | **String** | ISO currency, e.g. EUR, USD, GBP | [optional] |
| **language** | **String** | Locale, e.g. en-us, fr, de, es | [optional] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

