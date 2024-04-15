#### Parser Content
```Java
{
Name = "microsoft-evsecurity-str-user-password-modify-4723-1"
ParserVersion = v1.0.0
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """<EventID>4723</EventID>"""
  """An attempt was made to change an account's password"""
]
Fields = [
  """({event_name}An attempt was made to change an account's password)""",
  """SystemTime=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """<Computer>({host}[^<]+)</Computer>""",
  """<EventID>({event_code}[^<]+)</EventID>""",
  """<Keywords>({result}[^<]+)</Keywords>""",
  """Subject.+?Security ID:\s*({user_sid}.+?)\s*Account Name""",
  """Subject.+?Account Name:\s*({user}.+?)\s*Account Domain""",
  """Account Domain:\s*({domain}.+?)\s*Logon ID:\s*({login_id}.+?)\s*Target Account:""",
  """Target Account.+?Security ID:\s*({dest_user_sid}.+?)\s*Account Name:""",
  """Target Account.+?Account Name:\s*({dest_user}.+?)\s*Account Domain:\s*({dest_domain}.+?)\s*Additional"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```