#### Parser Content
```Java
{
Name = unix-unix-json-user-switch-success-sessionopenforuser
Product = "Unix"
Vendor = "Unix"
ExtractionType = json
Conditions = [
  """"type":"wazuh-alerts""""
  """session opened for user"""
  """(uid="""
  """sshd:"""
  """_unix"""
]
DupFields = [
  "host->dest_host"
  "user_uid->user_id"
  "description->event_name"
  "dest_user->account"
]
ParserVersion = "v1.0.0"


}
```