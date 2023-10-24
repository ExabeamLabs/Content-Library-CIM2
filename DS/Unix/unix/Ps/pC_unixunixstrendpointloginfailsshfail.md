#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-login-fail-sshfail
  ParserVersion = v1.0.0
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ssh: failed login attempt for """ ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+"""
    """Message forwarded from ({host}[^\s:]+)"""
    """({event_code}ssh)"""
    """failed login attempt for ({user}[\w\.\-]{1,40}\$?) from (({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))\s*"""
  ]
  ParserVersion = "v1.0.0"


}
```