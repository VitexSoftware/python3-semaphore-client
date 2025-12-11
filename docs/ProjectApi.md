# semaphore_client.ProjectApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**project_project_id_backup_get**](ProjectApi.md#project_project_id_backup_get) | **GET** /project/{project_id}/backup | Backup A Project
[**project_project_id_delete**](ProjectApi.md#project_project_id_delete) | **DELETE** /project/{project_id}/ | Delete project
[**project_project_id_events_get**](ProjectApi.md#project_project_id_events_get) | **GET** /project/{project_id}/events | Get Events related to this project
[**project_project_id_get**](ProjectApi.md#project_project_id_get) | **GET** /project/{project_id}/ | Fetch project
[**project_project_id_notifications_test_post**](ProjectApi.md#project_project_id_notifications_test_post) | **POST** /project/{project_id}/notifications/test | Send test notification
[**project_project_id_put**](ProjectApi.md#project_project_id_put) | **PUT** /project/{project_id}/ | Update project
[**project_project_id_role_get**](ProjectApi.md#project_project_id_role_get) | **GET** /project/{project_id}/role | Fetch permissions of the current user for project
[**project_project_id_users_get**](ProjectApi.md#project_project_id_users_get) | **GET** /project/{project_id}/users | Get users linked to project
[**project_project_id_users_post**](ProjectApi.md#project_project_id_users_post) | **POST** /project/{project_id}/users | Link user to project
[**project_project_id_users_user_id_delete**](ProjectApi.md#project_project_id_users_user_id_delete) | **DELETE** /project/{project_id}/users/{user_id} | Removes user from project
[**project_project_id_users_user_id_put**](ProjectApi.md#project_project_id_users_user_id_put) | **PUT** /project/{project_id}/users/{user_id} | Update user role
[**project_project_id_views_get**](ProjectApi.md#project_project_id_views_get) | **GET** /project/{project_id}/views | Get view
[**project_project_id_views_post**](ProjectApi.md#project_project_id_views_post) | **POST** /project/{project_id}/views | create view
[**project_project_id_views_view_id_delete**](ProjectApi.md#project_project_id_views_view_id_delete) | **DELETE** /project/{project_id}/views/{view_id} | Removes view
[**project_project_id_views_view_id_get**](ProjectApi.md#project_project_id_views_view_id_get) | **GET** /project/{project_id}/views/{view_id} | Get view
[**project_project_id_views_view_id_put**](ProjectApi.md#project_project_id_views_view_id_put) | **PUT** /project/{project_id}/views/{view_id} | Updates view
[**projects_get**](ProjectApi.md#projects_get) | **GET** /projects | Get projects
[**projects_post**](ProjectApi.md#projects_post) | **POST** /projects | Create a new project
[**projects_restore_post**](ProjectApi.md#projects_restore_post) | **POST** /projects/restore | Restore Project


# **project_project_id_backup_get**
> ProjectBackup project_project_id_backup_get(project_id)

Backup A Project

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.project_backup import ProjectBackup
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
    api_instance = semaphore_client.ProjectApi(api_client)
    project_id = 1 # int | Project ID

    try:
        # Backup A Project
        api_response = api_instance.project_project_id_backup_get(project_id)
        print("The response of ProjectApi->project_project_id_backup_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectApi->project_project_id_backup_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 

### Return type

[**ProjectBackup**](ProjectBackup.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Backup |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_delete**
> project_project_id_delete(project_id)

Delete project

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
    api_instance = semaphore_client.ProjectApi(api_client)
    project_id = 1 # int | Project ID

    try:
        # Delete project
        api_instance.project_project_id_delete(project_id)
    except Exception as e:
        print("Exception when calling ProjectApi->project_project_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 

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
**204** | Project deleted |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_events_get**
> List[Event] project_project_id_events_get(project_id)

Get Events related to this project

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.event import Event
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
    api_instance = semaphore_client.ProjectApi(api_client)
    project_id = 1 # int | Project ID

    try:
        # Get Events related to this project
        api_response = api_instance.project_project_id_events_get(project_id)
        print("The response of ProjectApi->project_project_id_events_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectApi->project_project_id_events_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 

### Return type

[**List[Event]**](Event.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Array of events in chronological order |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_get**
> Project project_project_id_get(project_id)

Fetch project

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.project import Project
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
    api_instance = semaphore_client.ProjectApi(api_client)
    project_id = 1 # int | Project ID

    try:
        # Fetch project
        api_response = api_instance.project_project_id_get(project_id)
        print("The response of ProjectApi->project_project_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectApi->project_project_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 

### Return type

[**Project**](Project.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Project |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_notifications_test_post**
> project_project_id_notifications_test_post(project_id)

Send test notification

Sends a test notification to all enabled messengers for the project

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
    api_instance = semaphore_client.ProjectApi(api_client)
    project_id = 1 # int | Project ID

    try:
        # Send test notification
        api_instance.project_project_id_notifications_test_post(project_id)
    except Exception as e:
        print("Exception when calling ProjectApi->project_project_id_notifications_test_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 

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
**409** | Alerts not enabled for the project |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_put**
> project_project_id_put(project_id, project_project_id_put_request)

Update project

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.project_project_id_put_request import ProjectProjectIdPutRequest
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
    api_instance = semaphore_client.ProjectApi(api_client)
    project_id = 1 # int | Project ID
    project_project_id_put_request = semaphore_client.ProjectProjectIdPutRequest() # ProjectProjectIdPutRequest | 

    try:
        # Update project
        api_instance.project_project_id_put(project_id, project_project_id_put_request)
    except Exception as e:
        print("Exception when calling ProjectApi->project_project_id_put: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **project_project_id_put_request** | [**ProjectProjectIdPutRequest**](ProjectProjectIdPutRequest.md)|  | 

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
**204** | Project saved |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_role_get**
> ProjectProjectIdRoleGet200Response project_project_id_role_get(project_id)

Fetch permissions of the current user for project

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.project_project_id_role_get200_response import ProjectProjectIdRoleGet200Response
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
    api_instance = semaphore_client.ProjectApi(api_client)
    project_id = 1 # int | Project ID

    try:
        # Fetch permissions of the current user for project
        api_response = api_instance.project_project_id_role_get(project_id)
        print("The response of ProjectApi->project_project_id_role_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectApi->project_project_id_role_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 

### Return type

[**ProjectProjectIdRoleGet200Response**](ProjectProjectIdRoleGet200Response.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Permissions |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_users_get**
> List[ProjectUser] project_project_id_users_get(project_id, sort, order)

Get users linked to project

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.project_user import ProjectUser
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
    api_instance = semaphore_client.ProjectApi(api_client)
    project_id = 1 # int | Project ID
    sort = 'email' # str | sorting name
    order = 'desc' # str | ordering manner

    try:
        # Get users linked to project
        api_response = api_instance.project_project_id_users_get(project_id, sort, order)
        print("The response of ProjectApi->project_project_id_users_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectApi->project_project_id_users_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **sort** | **str**| sorting name | 
 **order** | **str**| ordering manner | 

### Return type

[**List[ProjectUser]**](ProjectUser.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Users |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_users_post**
> project_project_id_users_post(project_id, project_project_id_users_post_request)

Link user to project

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.project_project_id_users_post_request import ProjectProjectIdUsersPostRequest
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
    api_instance = semaphore_client.ProjectApi(api_client)
    project_id = 1 # int | Project ID
    project_project_id_users_post_request = semaphore_client.ProjectProjectIdUsersPostRequest() # ProjectProjectIdUsersPostRequest | 

    try:
        # Link user to project
        api_instance.project_project_id_users_post(project_id, project_project_id_users_post_request)
    except Exception as e:
        print("Exception when calling ProjectApi->project_project_id_users_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **project_project_id_users_post_request** | [**ProjectProjectIdUsersPostRequest**](ProjectProjectIdUsersPostRequest.md)|  | 

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
**204** | User added |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_users_user_id_delete**
> project_project_id_users_user_id_delete(project_id, user_id)

Removes user from project

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
    api_instance = semaphore_client.ProjectApi(api_client)
    project_id = 1 # int | Project ID
    user_id = 2 # int | User ID

    try:
        # Removes user from project
        api_instance.project_project_id_users_user_id_delete(project_id, user_id)
    except Exception as e:
        print("Exception when calling ProjectApi->project_project_id_users_user_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **user_id** | **int**| User ID | 

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
**204** | User removed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_users_user_id_put**
> project_project_id_users_user_id_put(project_id, user_id, project_project_id_users_user_id_put_request)

Update user role

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.project_project_id_users_user_id_put_request import ProjectProjectIdUsersUserIdPutRequest
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
    api_instance = semaphore_client.ProjectApi(api_client)
    project_id = 1 # int | Project ID
    user_id = 2 # int | User ID
    project_project_id_users_user_id_put_request = semaphore_client.ProjectProjectIdUsersUserIdPutRequest() # ProjectProjectIdUsersUserIdPutRequest | 

    try:
        # Update user role
        api_instance.project_project_id_users_user_id_put(project_id, user_id, project_project_id_users_user_id_put_request)
    except Exception as e:
        print("Exception when calling ProjectApi->project_project_id_users_user_id_put: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **user_id** | **int**| User ID | 
 **project_project_id_users_user_id_put_request** | [**ProjectProjectIdUsersUserIdPutRequest**](ProjectProjectIdUsersUserIdPutRequest.md)|  | 

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
**204** | User updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_views_get**
> List[View] project_project_id_views_get(project_id)

Get view

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.view import View
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
    api_instance = semaphore_client.ProjectApi(api_client)
    project_id = 1 # int | Project ID

    try:
        # Get view
        api_response = api_instance.project_project_id_views_get(project_id)
        print("The response of ProjectApi->project_project_id_views_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectApi->project_project_id_views_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 

### Return type

[**List[View]**](View.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | view |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_views_post**
> View project_project_id_views_post(project_id, view_request)

create view

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.view import View
from semaphore_client.models.view_request import ViewRequest
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
    api_instance = semaphore_client.ProjectApi(api_client)
    project_id = 1 # int | Project ID
    view_request = semaphore_client.ViewRequest() # ViewRequest | 

    try:
        # create view
        api_response = api_instance.project_project_id_views_post(project_id, view_request)
        print("The response of ProjectApi->project_project_id_views_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectApi->project_project_id_views_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **view_request** | [**ViewRequest**](ViewRequest.md)|  | 

### Return type

[**View**](View.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | view created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_views_view_id_delete**
> project_project_id_views_view_id_delete(project_id, view_id)

Removes view

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
    api_instance = semaphore_client.ProjectApi(api_client)
    project_id = 1 # int | Project ID
    view_id = 10 # int | view ID

    try:
        # Removes view
        api_instance.project_project_id_views_view_id_delete(project_id, view_id)
    except Exception as e:
        print("Exception when calling ProjectApi->project_project_id_views_view_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **view_id** | **int**| view ID | 

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
**204** | view removed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_views_view_id_get**
> View project_project_id_views_view_id_get(project_id, view_id)

Get view

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.view import View
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
    api_instance = semaphore_client.ProjectApi(api_client)
    project_id = 1 # int | Project ID
    view_id = 10 # int | view ID

    try:
        # Get view
        api_response = api_instance.project_project_id_views_view_id_get(project_id, view_id)
        print("The response of ProjectApi->project_project_id_views_view_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectApi->project_project_id_views_view_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **view_id** | **int**| view ID | 

### Return type

[**View**](View.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | view object |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_project_id_views_view_id_put**
> project_project_id_views_view_id_put(project_id, view_id, view_request)

Updates view

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.view_request import ViewRequest
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
    api_instance = semaphore_client.ProjectApi(api_client)
    project_id = 1 # int | Project ID
    view_id = 10 # int | view ID
    view_request = semaphore_client.ViewRequest() # ViewRequest | 

    try:
        # Updates view
        api_instance.project_project_id_views_view_id_put(project_id, view_id, view_request)
    except Exception as e:
        print("Exception when calling ProjectApi->project_project_id_views_view_id_put: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **int**| Project ID | 
 **view_id** | **int**| view ID | 
 **view_request** | [**ViewRequest**](ViewRequest.md)|  | 

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
**204** | view updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projects_get**
> List[Project] projects_get()

Get projects

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.project import Project
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
    api_instance = semaphore_client.ProjectApi(api_client)

    try:
        # Get projects
        api_response = api_instance.projects_get()
        print("The response of ProjectApi->projects_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectApi->projects_get: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**List[Project]**](Project.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of projects |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projects_post**
> Project projects_post(project_request)

Create a new project

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.project import Project
from semaphore_client.models.project_request import ProjectRequest
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
    api_instance = semaphore_client.ProjectApi(api_client)
    project_request = semaphore_client.ProjectRequest() # ProjectRequest | 

    try:
        # Create a new project
        api_response = api_instance.projects_post(project_request)
        print("The response of ProjectApi->projects_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectApi->projects_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_request** | [**ProjectRequest**](ProjectRequest.md)|  | 

### Return type

[**Project**](Project.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created project |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projects_restore_post**
> Project projects_restore_post(project_backup)

Restore Project

### Example

* Api Key Authentication (cookie):
* Api Key Authentication (bearer):

```python
import semaphore_client
from semaphore_client.models.project import Project
from semaphore_client.models.project_backup import ProjectBackup
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
    api_instance = semaphore_client.ProjectApi(api_client)
    project_backup = semaphore_client.ProjectBackup() # ProjectBackup | 

    try:
        # Restore Project
        api_response = api_instance.projects_restore_post(project_backup)
        print("The response of ProjectApi->projects_restore_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectApi->projects_restore_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_backup** | [**ProjectBackup**](ProjectBackup.md)|  | 

### Return type

[**Project**](Project.md)

### Authorization

[cookie](../README.md#cookie), [bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain; charset=utf-8

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Created project |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

