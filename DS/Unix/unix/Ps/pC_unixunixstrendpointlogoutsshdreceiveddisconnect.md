#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-logout-sshdreceiveddisconnect"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [ 
    """ sshd"""
    """Received disconnect from"""
  ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """(::ffff:)?\d\d\s({host}[\w\-\.]+)(\s\w+)?\s*sshd"""
    """({time}\w+\s\d\d\s\d\d:\d\d:\d\d)? (::ffff:)?({host}[\w\-\.]+)?(\s\w+)?\s*sshd"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """Received disconnect from (::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """port ({src_port}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```