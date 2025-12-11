# EnvironmentSecret


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**name** | **str** |  | [optional] 
**type** | **str** |  | [optional] 

## Example

```python
from semaphore_client.models.environment_secret import EnvironmentSecret

# TODO update the JSON string below
json = "{}"
# create an instance of EnvironmentSecret from a JSON string
environment_secret_instance = EnvironmentSecret.from_json(json)
# print the JSON string representation of the object
print(EnvironmentSecret.to_json())

# convert the object into a dict
environment_secret_dict = environment_secret_instance.to_dict()
# create an instance of EnvironmentSecret from a dict
environment_secret_from_dict = EnvironmentSecret.from_dict(environment_secret_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


