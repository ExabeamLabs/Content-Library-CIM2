#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-logout-sshddisconnected"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","MMM dd HH:mm:ss"]
  Conditions = [ 
    """ sshd["""
    """Disconnected from user"""
  ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({time}\w+\s\d\d\s\d\d:\d\d:\d\d) (::ffff:)?({host}[\w\-\.]+)?(\s\w+)?\s*sshd""",
    """Disconnected from user (({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})) port ({src_port}\d+)""",
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  ParserVersion = "v1.0.0"


}
```