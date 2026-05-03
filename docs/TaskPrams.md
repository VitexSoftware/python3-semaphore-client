# TaskPrams


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**environment** | **str** |  | [optional] 
**git_branch** | **str** |  | [optional] 
**message** | **str** |  | [optional] 
**arguments** | **str** |  | [optional] 
**params** | [**TaskParams**](TaskParams.md) |  | [optional] 

## Example

```python
from semaphore_client.models.task_prams import TaskPrams

# TODO update the JSON string below
json = "{}"
# create an instance of TaskPrams from a JSON string
task_prams_instance = TaskPrams.from_json(json)
# print the JSON string representation of the object
print(TaskPrams.to_json())

# convert the object into a dict
task_prams_dict = task_prams_instance.to_dict()
# create an instance of TaskPrams from a dict
task_prams_from_dict = TaskPrams.from_dict(task_prams_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


