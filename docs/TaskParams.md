# TaskParams


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**debug** | **bool** |  | [optional] 
**dry_run** | **bool** |  | [optional] 
**diff** | **bool** |  | [optional] 
**limit** | **List[str]** |  | [optional] 
**tags** | **List[str]** |  | [optional] 
**skip_tags** | **List[str]** |  | [optional] 
**plan** | **bool** |  | [optional] 
**destroy** | **bool** |  | [optional] 
**auto_approve** | **bool** |  | [optional] 
**upgrade** | **bool** |  | [optional] 

## Example

```python
from semaphore_client.models.task_params import TaskParams

# TODO update the JSON string below
json = "{}"
# create an instance of TaskParams from a JSON string
task_params_instance = TaskParams.from_json(json)
# print the JSON string representation of the object
print(TaskParams.to_json())

# convert the object into a dict
task_params_dict = task_params_instance.to_dict()
# create an instance of TaskParams from a dict
task_params_from_dict = TaskParams.from_dict(task_params_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


