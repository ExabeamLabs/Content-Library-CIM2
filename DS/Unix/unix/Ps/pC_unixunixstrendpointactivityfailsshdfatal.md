#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-activity-fail-sshdfatal"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
    """<34>"""
    """sshd"""
    """ Message forwarded from """
    """fatal"""
  ]
  Fields = [
    """Message forwarded from ({host}[^\s:]+)"""
    """({event_code}sshd)"""
    """fatal: ({failure_reason}.*?)\s*$"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  ParserVersion = "v1.0.0"


}
```