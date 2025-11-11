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
    """({dest_host}({host}[^\s]+))\s+Detailed File Share""",
    """({event_code}5145)""",
    """SubjectUserName:({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)),""",
    """SubjectDomainName:({src_domain}({domain}[^,]+)),""",
    """SubjectLogonId:({login_id}[^,]+),""",
    """ObjectType:({file_type}[^,]+),""",
    """IpAddress:(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,""",
    """IpPort:({src_port}\d+),""",
    """ShareName:(?:\\\\\*\\)?({share_name}[^,]+),""",
    """ShareLocalPath:(|({share_path}(({d_parent}[^,]+?)\\)?(|({d_name}[^\\,]+?)))),""",
    """RelativeTargetName:({file_dir}(?:[^,]+)?[\\\/])?({file_name}[^\\:,]+?(\.\s*({file_ext}[^"\\.,]+?))?),""",
    """AccessList:({access}[^:]+),""",
    """({result}(Success|Failure) Audit)"""
    """Source Port(=|:)\s*({src_port}\d+)"""
  ]


}
```