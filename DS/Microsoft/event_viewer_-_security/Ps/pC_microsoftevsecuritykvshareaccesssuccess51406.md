#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-share-access-success-5140-6
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security 
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Microsoft-Windows-Security-Auditing""","""AccessList:""", """5140""", """AccessMask:""", """ObjectType:""", """ShareName:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d{1,3}""",
    """({host}[^\s]+?)\s+(Detailed File Share|File Share)""",
    """({event_code}5140)""",
    """SubjectUserName:({user}[\w\.\-\!\#\^\~]{1,40}\$?),""",
    """SubjectDomainName:({domain}[^,]+),""",
    """SubjectLogonId:({login_id}[^,]+),""",
    """ObjectType:({file_type}[^,]+),""",
    """IpAddress:(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,""",
    """IpPort:({src_port}\d+),""",
    """ShareName:(?:[\\\*]+)?({share_name}[^,]+),""",
    """ShareLocalPath:(|({share_path}(({d_parent}[^,]+?)\\)?(|({d_name}[^\\,]+?)))),""",
    """AccessList:({access}[^:]+),""",
    """({result}(Success|Failure) Audit)"""
    """Source Port(=|:)\s*({src_port}\d+)"""
  ]
  DupFields = ["host->dest_host"]


}
```