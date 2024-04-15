#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-switch-success-4648"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
"""4648""",
""""TargetServerName":"""
  ]
  Fields = [
"""({event_name}A logon was attempted using explicit credentials)""",
""""EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
"""\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s[^\s]+\s""",
""""EventReceivedTime":\s*({time}\d+)""",
""""timestamp":\s*({time}\d+)""",
""""(Hostname|MachineName|Computer)":"({host}[^"]*)""",
"""({event_code}4648)""",
""""SubjectUserSid":"({user_sid}[^"]*)""",
""""SubjectUserName":"(-|({user}[^"]*))""",
""""SubjectDomainName":"(-|({domain}[^"]*))""",
""""SubjectLogonId":"({login_id}[^"]*)""",
""""TargetUserName":"({dest_user}[^"]*)""",
""""TargetDomainName":"({dest_domain}[^\s"]*)""",
""""TargetServerName":"({dest_host}[^"]*)""",
""""TargetInfo":"({dest_service_name}[^"]*)""",
""""(?i)(ProcessId)":"*({process_id}[^",]*)""",
""""ProcessName":"(?: |({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+?)))"""",
""""IpAddress":"(?:-|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  ]
  DupFields = ["dest_user->account","dest_domain->account_domain"]


}
```