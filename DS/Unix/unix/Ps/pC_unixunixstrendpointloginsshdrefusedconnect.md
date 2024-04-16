#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-sshdrefusedconnect"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","MMM dd HH:mm:ss"]
  Conditions = [
    """ sshd["""
    """refused connect from"""
  ]
  Fields = [
    """({time}\w+\s*\d+ \d\d:\d\d:\d\d)? ({host}[\w.\-]+) sshd\["""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
    """refused connect from (({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}\S+))(\s+\(({=src_ip}[a-fA-F\d.:]+)\))?"""
  ]
  ParserVersion = "v1.0.0"


}
```