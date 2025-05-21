#### Parser Content
```Java
{
Name = "unix-unix-kv-endpoint-login-fail-logindenied"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [
    """ sshd["""
    """]: Login_Denied """
  ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d.\d\d\d)"""
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+"""
    """ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """auth=({event_name}[^\"\"]+)"""
    """apparentlyi_via=({login_type_text}[^\s]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```