#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-privilege-assign-success-4672"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
Conditions = [ """"EventID":4672""", """"PrivilegeList":"""" ]
Fields = [
  """({event_name}Special privileges assigned to new logon)""",
  """"EventReceivedTime":\s*({time}\d+)""",
  """"created":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """"Computer":"({host}({src_host}[\w\-.]+))"""",
  """"EventTime"*:"*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{7}Z)""",
  """"(Hostname|MachineName)":"({host}[\w\-.]*)""",
  """({event_code}4672)""",
  """"(Event|Entry)Type":"({result}[^"]+)""",
  """"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
  """"SubjectDomainName":"({src_domain}({domain}[^"]*))""",
  """"SubjectLogonId":"({login_id}[^"]*)""",
  """"PrivilegeList":"(-|({privileges}[^"]*))""",
  """"Keywords":"({result}[^\"]+)"""
]
ParserVersion = "v1.0.0"


}
```