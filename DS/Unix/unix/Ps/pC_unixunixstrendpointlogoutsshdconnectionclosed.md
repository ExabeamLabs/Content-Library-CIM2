#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-logout-sshdconnectionclosed"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","MMM dd HH:mm:ss"]
  Conditions = [ 
    """ sshd["""
    """Connection closed by"""
  ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """({time}\w+\s\d\d\s\d\d:\d\d:\d\d)? (::ffff:)?({host}[\w\-\.]+)(\s\w+)?\s*sshd"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
    """Connection closed by( authenticating user \S+)? ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"


}
```