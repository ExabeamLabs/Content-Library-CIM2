#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-logout-disconnected"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [
    """ sshd"""
    """Disconnected from"""
    ]
  Fields = [
    """\d\d:\d\d (::ffff:)?({host}[\w\-\.]+)(\s\w+)?\s*sshd"""
    """({time}\w+\s\d\d\s\d\d:\d\d:\d\d)? (::ffff:)?({host}[\w\-\.]+)(\s\w+)?\s*sshd"""
    """({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """ Disconnected from( authenticating user \S+)? (::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """ port ({src_port}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```