#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-add-success-memberadd"
ParserVersion = v1.0.0
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
  """A member was added to a security-enabled"""
  """EventID="""
  """EventIDCode="""
  """TimeGenerated="""
]
Fields = [
  """({event_name}A member was added to a security-enabled [\w\s]+ group)""",
  """EventID=({event_code}\d+)""",
  """TimeGenerated=({time}\d{10})""",
  """Computer=({host}[^\s]+)""",
  """A member was added to a security-enabled ({group_type}[^\s]+) group.+?Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?).+?Account Domain:\s*({domain}[^\s]+).+?Logon ID:\s*({login_id}[^\s]+)\s+""",
  """Member:\s*Security ID:\s*({account_id}.+?)\s*Account Name:""",
  """Member:\s*Security ID:\s*(({dest_user_sid}S-\d+-[^\s:]+)|({account_domain}[^\\]+)\\({account_name}.+?)|(?:[^\s]+))\s*Account Name:""",
  """Member:.*?Account Name:\s*(?:-|({user_dn}(CN|cn)=.+?,({user_ou}(OU|ou).+?(DC|dc)=[\w-]+)))?\s*Group:\s*Security ID:\s*({group_id}.+?)\s*(Group|Account) Name:\s*({group_name}.+?)?\s*(Group|Account) Domain:\s*({group_domain}.+?)\s*Additional Information:"""
]
DupFields = [
  "host->dest_host"
  "account_id->member"
]
ParserVersion = "v1.0.0"


}
```