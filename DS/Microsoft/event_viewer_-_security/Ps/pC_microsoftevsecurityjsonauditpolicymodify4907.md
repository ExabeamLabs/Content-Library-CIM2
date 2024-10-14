#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-audit-policy-modify-4907
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"EventID":4907""", """Auditing settings on object were changed""" ]
  Fields = [
    """"Hostname"+:"+({host}[^",]+)""",
    """"EventTime"+:"+({time}[^",]+)""",
    """({event_code}4907)""",
    """({event_name}Auditing settings on object were changed)""",
    """"SubjectUserSid"+:"+({user_sid}[^"]+)""",
    """"SubjectUserName"+:"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """"SubjectDomainName"+:"+({domain}[^"]+)""",
    """"SubjectLogonId"+:"+({login_id}[^"]+)""",
    """"ObjectServer"+:"+({object_server}[^"]+)""",
    """"ObjectType"+:"+({object_type}[^"]+)""",
    """"ObjectName"+:"+({object}[^"]+)""",
    """"HandleId"+:"+({handle_id}[^"]+)""",
    """"ProcessId"+:"+({process_id}[^"]+)""",
    """"ProcessName"+:"+({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))""""
    """New Security Descriptor:(\\t|\\r|\\n)*[^\S<]*({audit_policy_name}[^<"]+?)(\s+|<|")"""
  ]


}
```