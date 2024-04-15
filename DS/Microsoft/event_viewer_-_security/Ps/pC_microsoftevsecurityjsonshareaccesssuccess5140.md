#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-share-access-success-5140"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [ """A network share object was accessed""", """"EventID":5140""" ]
Fields = [
  """({event_name}A network share object was accessed)""",
  """({event_code}5140)""",
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)"""",
  """"Computer":"({host}[^"]+)"""",
  """"Hostname":"({host}[^"]+)"""",
  """"EventTime":({time}\d+)""",
  """"EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
  """"SubjectUserSid":"({user_sid}[^"]+)"""",
  """"SubjectUserName":"({user}[^"]+)"""",
  """"SubjectDomainName":"({domain}[^"]+)"""",
  """"SubjectLogonId":"({login_id}[^"]+)"""",
  """"ObjectType":"({file_type}[^"]+)"""",
  """IpAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """"IpPort":"({src_port}\d+)"""",
  """"ShareName":"[\\*]*({share_name}[^"]+)"""",
  """({access}Read)""",
  """"ShareLocalPath":"[\\?]*(({share_path}(({d_parent}.+?)[\\\/])?(|({d_name}[^\\\/]+?)))[\\\/]?)","""
  """"ProcessID":({process_id}\d+),""",
  """"RecordNumber":({event_id}\d+),""",
  """"Category":"({service_name}[^"]+)","""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```