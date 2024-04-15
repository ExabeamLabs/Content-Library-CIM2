#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-switch-success-4648"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""<EventID>4648</EventID>""",
"""='ProcessName'"""
  ]
  Fields = [
"""SystemTime=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
"""<Computer>({host}[^<]+)</Computer>""",
"""<EventID>({event_code}\d+)</EventID>""",
"""<Data Name ='SubjectUserSid'>({user_sid}[^<]+)<\/Data>""",
"""<Data Name ='SubjectUserName'>(-|({user}[^<]+))</Data>""",
"""<Data Name ='SubjectDomainName'>(-|({domain}[^<]+))</Data>""",
"""<Data Name ='SubjectLogonId'>({login_id}[^<]+)</Data>""",
"""<Data Name ='TargetUserName'>({dest_user}[^<]+?)\s*</Data>""",
"""<Data Name ='TargetDomainName'>({dest_domain}[^<]+)</Data>""",
"""<Data Name ='TargetServerName'>({dest_host}[\w\-]+)[^<]*</Data>""",
"""<Data Name ='ProcessId'>({process_id}[^<]+)</Data>""",
"""<Data Name ='ProcessName'>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/\"]+?))<\/Data>""",
"""<Data Name ='IpAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</Data>""",
"""<Data Name ='TargetInfo'>({dest_service_name}[^<]+)</Data>""",
"""<Message>({event_name}A logon was attempted using explicit credentials)"""
  ]
   DupFields = ["dest_user->account", "dest_domain->account_domain"]


}
```