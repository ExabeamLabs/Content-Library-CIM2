#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-fail-manyauthfail"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """Disconnecting: Too many authentication failures for"""
  ]
  Fields = [
    """({dest_host}({host}[\w.\-]+))\s+sshd\["""
    """({failure_reason}({event_name}Too many authentication failures)) for ({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """({event_code}ssh)"""
    """\[\]:\s\w{3} \d\d \d\d:\d\d:\d\d ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  ParserVersion = "v1.0.0"


}
```