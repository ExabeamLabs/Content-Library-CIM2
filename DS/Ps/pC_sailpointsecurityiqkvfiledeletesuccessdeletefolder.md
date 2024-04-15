#### Parser Content
```Java
{
Name = "sailpoint-securityiq-kv-file-delete-success-deletefolder"
Conditions = [
  """| applicationtype : Netapp - CIFS |"""
  """actiontype : Delete Folder"""
]
DupFields = [
  "event_name->access"
]
ParserVersion = "v1.0.0"


}
```