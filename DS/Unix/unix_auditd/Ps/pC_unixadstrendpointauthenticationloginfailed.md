#### Parser Content
```Java
{
Name = unix-ad-str-endpoint-authentication-loginfailed
  Vendor = Unix
  Product = Unix Auditd
  ParserVersion = v1.0.0
  TimeFormat = "epoch_sec"
  Conditions = [ """- USER""","""(Login failed):""" ]
  Fields = [
    """USER\s*({user}[\w\.\-]{1,40}\$?)"""
    """\d\d:\d\d:\d\d(\.\S+)?\s({host}[^\s]+)"""
    """({src_host}[\w\-.]+)\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\]\)"""
    """\(Login\s*({result}[^\):]+)"""
  ]


}
```