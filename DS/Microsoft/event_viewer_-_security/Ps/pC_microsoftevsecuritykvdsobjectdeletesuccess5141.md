#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-ds-object-delete-success-5141"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["MMM dd HH:mm:ss yyyy", "MM/dd/yyyy hh:mm:ss a"]
Conditions = [ """A directory service object was deleted""", """Account Name:""" ]
Fields = [
  """({event_name}A directory service object was deleted)""",
  """({time}\w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+""",
  """({event_code}5141)""",
  """\s(?i)(success|failure|audit)\s+\w+\s+({host}[\w\-.]+)""",
  """Subject:.+?Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:\s+({domain}.+?)\s+Logon ID:\s+({login_id}[^\s]+)""",
  """Object:.+?Class:\s+({object_type}.+?)\s+Operation:""",
  """Object:\s+DN:\s+({ds_object_dn}.+?)\s+GUID:""",
  """Object:\s+DN:.+?({ds_object_ou}OU.+?)\s+GUID:""",
  """Account Name:\s*(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:\s*(|({domain}[^\s]+))\s+Logon ID:\s*(|({login_id}[^\s]+))\s+Target Account:""",
  """Target\sAccount.+?Security ID:\s*({dest_user_sid}[^\s]+)\s""",
  """Target\sAccount.+?Account Name:\s*({dest_user}[^\s]+)\s""",
  """Target\sAccount.+?Account Domain:\s*({dest_domain}[^\s]+)\s""",
  """User Account Control:\s*.+?\-\s({status_msg}[^\s]+)\s""",
  """Changed Attributes:\s*(|({attribute}[^\s]+))\s+SAM Account Name""",
  """Directory Service:\s*Name(:|=)\s*({ds_name}[^\s]+)\s*.*?Type(:|=)\s*({ds_type}.*?Services)"""
  """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
]
ParserVersion = "v1.0.0"


}
```