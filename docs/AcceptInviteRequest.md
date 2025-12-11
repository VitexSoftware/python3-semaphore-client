# AcceptInviteRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **str** | The invitation token | 

## Example

```python
from semaphore_client.models.accept_invite_request import AcceptInviteRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AcceptInviteRequest from a JSON string
accept_invite_request_instance = AcceptInviteRequest.from_json(json)
# print the JSON string representation of the object
print(AcceptInviteRequest.to_json())

# convert the object into a dict
accept_invite_request_dict = accept_invite_request_instance.to_dict()
# create an instance of AcceptInviteRequest from a dict
accept_invite_request_from_dict = AcceptInviteRequest.from_dict(accept_invite_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


