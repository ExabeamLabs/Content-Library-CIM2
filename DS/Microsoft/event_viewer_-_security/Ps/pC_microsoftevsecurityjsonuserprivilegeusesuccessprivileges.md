#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-privilege-use-success-privileges"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
  """Special privileges assigned to new logon"""
  """"subject-AccountName":"""
  """"privileges":"""
]
Fields = [
  """({event_name}Special privileges assigned to new logon)"""
  """"subject-AccountName\":\"({user}[\w\.\-]{1,40}\$?)"""
  """"level\":\"({result}[^\"]+)"""
  """"time\":\"({time}\d+\/\d+\/\d\d\d\d \d+:\d\d:\d\d (am|AM|pm|PM))"""
  """"privileges\":\[({privileges}.+?)\]"""
  """"subject-LogonID\":\"({login_id}[^\"]+)"""
  """"subject-AccountDomain\":\"({domain}[^\"]+)"""
  """"subject-SecurityID\":\"({user_sid}[^\"]+)"""
  """"event_id\":\"({event_code}\d+)"""
  """"computer\":\"({host}[\w\-.]+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```