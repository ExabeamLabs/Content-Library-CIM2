#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-4776-2"
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Microsoft-Windows-Security-Auditing""", """Credential Validation""", """4776""", """TargetUserName:""", """PackageName:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d{1,3}""",
    """({host}[^\s]+)\s+Credential Validation""",
    """({event_code}4776)""",
    """TargetUserName:(({dest_user}[^@,]+@[^,]+)|({user}[^,]+)),\s+\w+""",
    """Workstation:[\\]*(({src_ip}[a-fA-F.:\d]+)|({src_host}[^,]+)),""",
    """PackageName:({auth_package}[^,]+?),""",
    """Status:({result_code}[^,\s]+?)\s+"""
  ]
  DupFields = [
   "host->dest_host"
  ]

  ParserVersion = "v1.0.0"


}
```