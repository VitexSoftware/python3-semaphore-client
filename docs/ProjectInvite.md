# ProjectInvite


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**project_id** | **int** |  | [optional] 
**user_id** | **int** | User ID for user-based invites (optional) | [optional] 
**email** | **str** | Email address for email-based invites (optional) | [optional] 
**role** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**inviter_user_id** | **int** | ID of the user who created the invite | [optional] 
**created** | **datetime** | When the invite was created | [optional] 
**expires_at** | **datetime** | When the invite expires (optional) | [optional] 
**accepted_at** | **datetime** | When the invite was accepted (optional) | [optional] 
**inviter_user** | [**User**](User.md) |  | [optional] 
**user** | [**User**](User.md) |  | [optional] 

## Example

```python
from semaphore_client.models.project_invite import ProjectInvite

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectInvite from a JSON string
project_invite_instance = ProjectInvite.from_json(json)
# print the JSON string representation of the object
print(ProjectInvite.to_json())

# convert the object into a dict
project_invite_dict = project_invite_instance.to_dict()
# create an instance of ProjectInvite from a dict
project_invite_from_dict = ProjectInvite.from_dict(project_invite_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


