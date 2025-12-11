# semaphore_client.InventoryApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**project_project_id_inventory_get**](InventoryApi.md#project_project_id_inventory_get) | **GET** /project/{project_id}/inventory | Get inventory
[**project_project_id_inventory_inventory_id_delete**](InventoryApi.md#project_project_id_inventory_inventory_id_delete) | **DELETE** /project/{project_id}/inventory/{inventory_id} | Removes inventory
[**project_project_id_inventory_inventory_id_get**](InventoryApi.md#project_project_id_inventory_inventory_id_get) | **GET** /project/{project_id}/inventory/{inventory_id} | Get inventory
[**project_project_id_inventory_inventory_id_put**](InventoryApi.md#project_project_id_inventory_inventory_id_put) | **PUT** /project/{project_id}/inventory/{inventory_id} | Updates inventory
[**project_project_id_inventory_post**](InventoryApi.md#project_project_id_inventory_post) | **POST** /project/{project_id}/inventory | create inventory


# **project_project_id_inventory_get**
> List[Inventory] project_project_id_inventory_get(project_id, sort, order)

Get inventory

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.inventory import Inventory
from semaphore_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /api
# See configuration.py for a list of all supported configuration parameters.
configuration = semaphore_client.Configuration(
    host = "/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: cookie
configuration.api_key['cookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['cookie'] = 'Bearer'

# Configure API key authorization: bearer
configuration.api_key['bearer'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['bearer'] = 'Bearer'

# Enter a context with an instance of the API client
with semaphore_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = semaphore_client.InventoryApi(api_client)
    project_id = 1 # int | Project ID
    sort = 'sort_example' # str | sorting name
    order = 'order_example' # str | ordering manner

    try:
        # Get inventory
        api_response = api_instance.project_project_id_inventory_get(project_id, sort, order)
        print("The response of InventoryApi->project_project_id_inventory_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InventoryApi->project_project_id_inventory_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **sort** | **str**| sorting name | 
 **order** | **str**| ordering manner | 

### Return type

[**List[Inventory]**](Inventory.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | inventory |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_inventory_inventory_id_delete**
> project_project_id_inventory_inventory_id_delete(project_id, inventory_id)

Removes inventory

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /api
# See configuration.py for a list of all supported configuration parameters.
configuration = semaphore_client.Configuration(
    host = "/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: cookie
configuration.api_key['cookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['cookie'] = 'Bearer'

# Configure API key authorization: bearer
configuration.api_key['bearer'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['bearer'] = 'Bearer'

# Enter a context with an instance of the API client
with semaphore_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = semaphore_client.InventoryApi(api_client)
    project_id = 1 # int | Project ID
    inventory_id = 5 # int | inventory ID

    try:
        # Removes inventory
        api_instance.project_project_id_inventory_inventory_id_delete(project_id, inventory_id)
    except Exception as e:
        print("Exception when calling InventoryApi->project_project_id_inventory_inventory_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **inventory_id** | **int**| inventory ID | 

### Return type

void (empty response body)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | inventory removed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_inventory_inventory_id_get**
> Inventory project_project_id_inventory_inventory_id_get(project_id, inventory_id)

Get inventory

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.inventory import Inventory
from semaphore_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /api
# See configuration.py for a list of all supported configuration parameters.
configuration = semaphore_client.Configuration(
    host = "/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: cookie
configuration.api_key['cookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['cookie'] = 'Bearer'

# Configure API key authorization: bearer
configuration.api_key['bearer'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['bearer'] = 'Bearer'

# Enter a context with an instance of the API client
with semaphore_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = semaphore_client.InventoryApi(api_client)
    project_id = 1 # int | Project ID
    inventory_id = 5 # int | inventory ID

    try:
        # Get inventory
        api_response = api_instance.project_project_id_inventory_inventory_id_get(project_id, inventory_id)
        print("The response of InventoryApi->project_project_id_inventory_inventory_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InventoryApi->project_project_id_inventory_inventory_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **inventory_id** | **int**| inventory ID | 

### Return type

[**Inventory**](Inventory.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | inventory object |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_inventory_inventory_id_put**
> project_project_id_inventory_inventory_id_put(project_id, inventory_id, inventory_request)

Updates inventory

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.inventory_request import InventoryRequest
from semaphore_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /api
# See configuration.py for a list of all supported configuration parameters.
configuration = semaphore_client.Configuration(
    host = "/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: cookie
configuration.api_key['cookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['cookie'] = 'Bearer'

# Configure API key authorization: bearer
configuration.api_key['bearer'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['bearer'] = 'Bearer'

# Enter a context with an instance of the API client
with semaphore_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = semaphore_client.InventoryApi(api_client)
    project_id = 1 # int | Project ID
    inventory_id = 5 # int | inventory ID
    inventory_request = semaphore_client.InventoryRequest() # InventoryRequest | 

    try:
        # Updates inventory
        api_instance.project_project_id_inventory_inventory_id_put(project_id, inventory_id, inventory_request)
    except Exception as e:
        print("Exception when calling InventoryApi->project_project_id_inventory_inventory_id_put: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **inventory_id** | **int**| inventory ID | 
 **inventory_request** | [**InventoryRequest**](InventoryRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Inventory updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_inventory_post**
> Inventory project_project_id_inventory_post(project_id, inventory_request)

create inventory

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.inventory import Inventory
from semaphore_client.models.inventory_request import InventoryRequest
from semaphore_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /api
# See configuration.py for a list of all supported configuration parameters.
configuration = semaphore_client.Configuration(
    host = "/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: cookie
configuration.api_key['cookie'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['cookie'] = 'Bearer'

# Configure API key authorization: bearer
configuration.api_key['bearer'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['bearer'] = 'Bearer'

# Enter a context with an instance of the API client
with semaphore_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = semaphore_client.InventoryApi(api_client)
    project_id = 1 # int | Project ID
    inventory_request = semaphore_client.InventoryRequest() # InventoryRequest | 

    try:
        # create inventory
        api_response = api_instance.project_project_id_inventory_post(project_id, inventory_request)
        print("The response of InventoryApi->project_project_id_inventory_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InventoryApi->project_project_id_inventory_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **inventory_request** | [**InventoryRequest**](InventoryRequest.md)|  | 

### Return type

[**Inventory**](Inventory.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | inventory created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

