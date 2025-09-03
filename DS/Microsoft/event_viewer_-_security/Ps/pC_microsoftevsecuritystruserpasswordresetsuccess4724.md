#### Parser Content
```Java
{
Name = "microsoft-evsecurity-str-user-password-reset-success-4724"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """<EventID>4724</EventID>"""
  """An attempt was made to reset an account's password"""
]
Fields = [
  """({event_name}An attempt was made to reset an account's password)""",
  """SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
  """<EventID>({event_code}[^<]+)</EventID>""",
  """Subject:.*?Security ID:\s*({user_sid}.+?)\s*Account Name:""",
  """Subject:.*?Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Account Domain:\s*({domain}.+?)\s*Logon ID:\s*({login_id}[^\s]+?)\s*Target Account""",
  """Target Account:.*?Security ID:\s*({dest_user_sid}.+?)\s*Account Name:\s*(?=\w)({dest_user}.+?)\s*Account Domain:\s*(?=\w)({dest_domain}[^",\s<]+)"""
]
ParserVersion = "v1.0.0"


}
```