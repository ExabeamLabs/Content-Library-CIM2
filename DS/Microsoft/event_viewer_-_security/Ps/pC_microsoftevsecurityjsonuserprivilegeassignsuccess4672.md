#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-privilege-assign-success-4672"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """4672""", """"PrivilegeList":"""" ]
Fields = [
  """({event_name}Special privileges assigned to new logon)""",
  """"EventReceivedTime":\s*({time}\d+)""",
  """"TimeCreated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """"Computer":"({host}[\w\-.]+)"""",
  """"EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """"(Hostname|MachineName)":"({host}[\w\-.]*)""",
  """({event_code}4672)""",
  """"(Event|Entry)Type":"({result}[^"]+)""",
  """"SubjectUserName":"({user}[\w\.\-]{1,40}\$?)""",
  """"SubjectDomainName":"({domain}[^"]*)""",
  """"SubjectLogonId":"({login_id}[^"]*)""",
  """"PrivilegeList":"(-|({privileges}[^"]*))""",
  """"Keywords":"({result}[^\"]+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```