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
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
  """"Computer":"({host}[\w\-.]+)"""",
  """"ComputerName":"({host}[\w\-.]+)""""
  """"Hostname":"({host}[\w\-.]+)"""",
  """"EventTime":({time}\d+)""",
  """"EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
  """Security ID:\s*(\\t|\\r|\\n)*({user_sid}[^\s\\"]+)\s*(\\t|\\r|\\n)*Account Name:\s*(\\t|\\r|\\n)*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(\\t|\\r|\\n)*Account Domain:\s*(\\t|\\r|\\n)*({domain}[^\s\\"]+)\s*(\\t|\\r|\\n)*Logon ID:\s*(\\t|\\r|\\n)*({login_id}[^\s"\\]+)\s*(\\t|\\r|\\n)*"""
  """Object Type:\s*(\\t|\\r|\\n)*({file_type}[^\\"\s]+)\s*(\\t|\\r|\\n)*Source Address:"""
  """Source Address:\s*(\\t|\\r|\\n)*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s*(\\t|\\r|\\n)*Source Port:\s*(\\t|\\r|\\n)*({src_port}\d+)\s*(\\t|\\r|\\n)*"""
  """Share Path:\s*(\\t|\\r|\\n)*[\\\?]*({share_path}(({d_parent}[^@]+?)\\*)?(|({d_name}[^\\]+?)))\s*(\\t|\\r|\\n)*Access Request Information:"""
  """Share Name:\s*(\\t|\\r|\\n)*[\\\*]*({share_name}[^\s\\]+)\s*(\\t|\\r|\\n)*Share Path:"""
  """"SubjectUserSid":"({user_sid}[^"]+)"""",
  """"SubjectUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
  """"SubjectDomainName":"({domain}[^"]+)"""",
  """"SubjectLogonId":"({login_id}[^"]+)"""",
  """"ObjectType":"({file_type}[^"]+)"""",
  """IpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """"IpPort":"({src_port}\d+)"""",
  """"ShareName":"(?:[\\\*]+)?({share_name}[^"]+)"""",
  """({access}Read)""",
  """"ShareLocalPath":"[\\?]*(({share_path}(({d_parent}.+?)[\\\/])?(|({d_name}[^\\\/]+?)))[\\\/]?)","""
  """"ProcessID":({process_id}\d+),""",
  """"RecordNumber":({event_id}\d+),""",
  """"Category":"({service_name}[^"]+)","""
  """Source Port(=|:)\s*(\\t)*({src_port}\d+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```