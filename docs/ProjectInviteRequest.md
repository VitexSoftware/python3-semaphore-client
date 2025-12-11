# ProjectInviteRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** | Email address to invite (use either user_id or email, not both) | [optional] 
**role** | **str** |  | 
**expires_at** | **datetime** | When the invite should expire (optional, defaults to 7 days) | [optional] 

## Example

```python
from semaphore_client.models.project_invite_request import ProjectInviteRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectInviteRequest from a JSON string
project_invite_request_instance = ProjectInviteRequest.from_json(json)
# print the JSON string representation of the object
print(ProjectInviteRequest.to_json())

# convert the object into a dict
project_invite_request_dict = project_invite_request_instance.to_dict()
# create an instance of ProjectInviteRequest from a dict
project_invite_request_from_dict = ProjectInviteRequest.from_dict(project_invite_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


