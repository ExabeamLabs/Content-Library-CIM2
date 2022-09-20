#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-share-access-5145
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security 
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Detailed File Share""", """Microsoft-Windows-Security-Auditing""","""RelativeTargetName:""", """AccessList:""", """5145""", """AccessMask:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d{1,3}[+\-]+\d\d:\d\d""",
    """({host}[^\s]+)\s+Detailed File Share""",
    """({event_code}5145)""",
    """SubjectUserName:({user}[^,]+),""",
    """SubjectDomainName:({domain}[^,]+),""",
    """SubjectLogonId:({login_id}[^,]+),""",
    """ObjectType:({file_type}[^,]+),""",
    """IpAddress:(::ffff:)?({src_ip}[a-fA-F\d:.]+),""",
    """IpPort:({src_port}\d+),""",
    """ShareName:(?:\\\\\*\\)?({share_name}[^,]+),""",
    """ShareLocalPath:(|({share_path}(({d_parent}[^,]+?)\\)?(|({d_name}[^\\,]+?)))),""",
    """RelativeTargetName:({f_parent}(?:[^,]+)?[\\\/])?({file_name}[^\\:,]+?(\.\s*({file_ext}[^"\\.,]+?))?),""",
    """AccessList:({access}[^:]+),""",
    """({result}(Success|Failure) Audit)"""
  ]
  DupFields = ["host->dest_host"]


}
```