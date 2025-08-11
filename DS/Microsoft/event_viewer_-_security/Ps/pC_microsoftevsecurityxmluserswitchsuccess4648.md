#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-switch-success-4648"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Conditions = [
"""<EventID>4648</EventID>""",
"""ProcessName""",
"""<Data Name""",
"""</Data>"""
  ]
  Fields = [
"""SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
"""SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7,9}Z)""",
"""<EventID>({event_code}\d+)</EventID>""",
"""<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^<]+)<\/Data>""",
"""<Data Name\\*=('|")SubjectUserName('|")>\s*(-|(?i)(anonymous logon|LOCAL SERVICE)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*</Data>""",
"""<Data Name\\*=('|")SubjectDomainName('|")>(-|({domain}[^<]+))</Data>""",
"""<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)</Data>""",
"""<Data Name\\*=('|")TargetUserName('|")>(({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({dest_user}[^@",\s<]+)@?({dest_domain}[^\\<]+)?))\s*<\/Data>""",
"""<Data Name\\*=('|")TargetDomainName('|")>(?=\w)({dest_domain}[^<]+?)</Data>""",
"""<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
"""<Data Name\\*=('|")TargetServerName('|")>(localhost|({dest_host}[\w\-.]+))[^<]*</Data>""",
"""<Data Name\\*=('|")ProcessId('|")>({process_id}[^<]+)</Data>""",
"""<Data Name\\*=('|")ProcessName('|")>(-|({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/\"]+?)))<\/Data>""",
"""<Data Name\\*=('|")IpAddress('|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</Data>""",
"""<Data Name\\*=('|")TargetInfo('|")>({dest_service_name}[^<]+)</Data>""",
"""<Message>({event_name}A logon was attempted using explicit credentials)""",
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
"""<Opcode>({result_code}\d+)<""",
"""<Keyword>({result}[^<]+)</Keyword>""",
"""<Level>({run_level}[^<]+)<"""
  ]
   DupFields = ["dest_user->account", "dest_domain->account_domain", "user->src_user" , "domain->src_domain"]


}
```