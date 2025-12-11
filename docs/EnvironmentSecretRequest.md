# EnvironmentSecretRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**name** | **str** |  | [optional] 
**secret** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**operation** | **str** |  | [optional] 

## Example

```python
from semaphore_client.models.environment_secret_request import EnvironmentSecretRequest

# TODO update the JSON string below
json = "{}"
# create an instance of EnvironmentSecretRequest from a JSON string
environment_secret_request_instance = EnvironmentSecretRequest.from_json(json)
# print the JSON string representation of the object
print(EnvironmentSecretRequest.to_json())

# convert the object into a dict
environment_secret_request_dict = environment_secret_request_instance.to_dict()
# create an instance of EnvironmentSecretRequest from a dict
environment_secret_request_from_dict = EnvironmentSecretRequest.from_dict(environment_secret_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


