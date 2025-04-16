#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-file-read-success-4663-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ParserVersion = "v1.0.0"
  Conditions = [ """Success Audit""", """ProcessName:""", """Microsoft-Windows-Security-Auditing""", """4663""", """SubjectUserName:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}[+-]\d\d:\d\d)\s\S+\sMSWinEventLog""",
    """(::ffff:)?({host}[\w.-]+)\s\d{1,3}\s\d\d\d\d-\d\d-\d\d""",
    """({event_code}4663)""",
    """SubjectUserSid:({user_sid}[^\s,]+),""",
    """SubjectUserName:({user}[\w\.\-\!\#\^\~]{1,40}\$?),""",
    """SubjectDomainName:({domain}[^:,]+?),""",
    """SubjectLogonId:({login_id}[^\s,]+),""",
    """ObjectServer:({object_server}[^\s,]+),""",
    """ObjectType:({file_type}[^\s,]+),""",
    """ObjectName:(|({registry_path}\\+REGISTRY[^:]+?(\\\{({registry_key}[^\}:]+)\})?)|({file_path}({file_dir}[^,]+?)[\\\/]+({file_name}[^\\\/;,]+?(\.({file_ext}[^\.\\\/;,]+?))?)))\s*,""",
    """AccessList:({access}[^,]+?),""",
    """AccessMask:({access_mask}[^,]+?),""",
    """ProcessName:(|({process_path}({process_dir}(?:[^";,]+?))?[\\\/]+?({process_name}[^\\\/";,]+?)))\s*,"""
  ]
  DupFields = ["user->src_user", "domain->src_domain"]


}
```