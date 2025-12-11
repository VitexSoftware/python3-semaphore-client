# AnsibleTaskParams


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**debug** | **bool** |  | [optional] 
**dry_run** | **bool** |  | [optional] 
**diff** | **bool** |  | [optional] 
**limit** | **List[str]** |  | [optional] 
**tags** | **List[str]** |  | [optional] 
**skip_tags** | **List[str]** |  | [optional] 

## Example

```python
from semaphore_client.models.ansible_task_params import AnsibleTaskParams

# TODO update the JSON string below
json = "{}"
# create an instance of AnsibleTaskParams from a JSON string
ansible_task_params_instance = AnsibleTaskParams.from_json(json)
# print the JSON string representation of the object
print(AnsibleTaskParams.to_json())

# convert the object into a dict
ansible_task_params_dict = ansible_task_params_instance.to_dict()
# create an instance of AnsibleTaskParams from a dict
ansible_task_params_from_dict = AnsibleTaskParams.from_dict(ansible_task_params_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


