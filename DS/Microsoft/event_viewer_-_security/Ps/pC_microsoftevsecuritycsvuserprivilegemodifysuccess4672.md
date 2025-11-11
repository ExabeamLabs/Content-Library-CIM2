#### Parser Content
```Java
{
Name = microsoft-evsecurity-csv-user-privilege-modify-success-4672
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Microsoft-Windows-Security-Auditing""", """Special Logon""", """4672""", """PrivilegeList:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d{1,3}[+\-]+\d\d:\d\d""",
    """({host}[^\s]+)\s+Special Logon""",
    """({event_code}4672)""",
    """SubjectUserName:({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)),""",
    """SubjectDomainName:({src_domain}({domain}[^,]+)),""",
    """SubjectLogonId:({login_id}[^,]+),""",
    """PrivilegeList:({privileges}[^\d]+?)\s\d+""",
    """({result}(Success|Failure) Audit)"""
  ]


}
```