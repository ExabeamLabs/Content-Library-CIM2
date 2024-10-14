#### Parser Content
```Java
{
Name = microsoft-evsecurity-csv-user-privilege-use-success-4673
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Microsoft-Windows-Security-Auditing""", """PrivilegeList:""", """4673""", """ObjectServer:""", """Sensitive Privilege Use""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d{1,3}[+\-]+\d\d:\d\d""",
    """({host}[^\s]+)\s+Sensitive Privilege Use""",
    """({event_code}4673)""",
    """SubjectUserName:({user}[\w\.\-\!\#\^\~]{1,40}\$?),""",
    """SubjectDomainName:({domain}[^,]+),""",
    """SubjectLogonId:({login_id}[^,]+),""",
    """PrivilegeList:({privileges}[^:]+),\s+\w+:""",
    """ProcessId:({process_id}[^,]+),""",
    """ProcessName:({process_path}(({process_dir}[^"]+)[\\\/])?({process_name}[^"\\]+?))\s+\d+""",
    """({result}(Success|Failure) Audit)"""
  ]


}
```