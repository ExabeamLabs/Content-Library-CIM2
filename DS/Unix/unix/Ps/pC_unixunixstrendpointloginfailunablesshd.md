#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-fail-unablesshd"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """ sshd["""
    """]: Unable to negotiate """
  ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-\.]+)))\s+"""
    """Unable to negotiate with (({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})|({src_host}[^\s]+))"""
    """ port ({src_port}\d+)(:\s+)?({failure_reason}.+?)\.\s"""
  ]
  ParserVersion = "v1.0.0"


}
```