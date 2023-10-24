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
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+"""
    """Unable to negotiate with (({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})|({dest_host}[^\s]+))"""
    """ port ({src_port}\d+)(:\s+)?({failure_reason}.+?)\.\s"""
  ]
  DupFields = [
"host->src_host"
]
  ParserVersion = "v1.0.0"


}
```