#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-logout-sshdreceiveddisconnect"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
    """ sshd["""
    """Received disconnect from"""
  ]
  Fields = [
    """(::ffff:)?({host}[\w.\-]+):? sshd\["""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
    """Received disconnect from (::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """port ({src_port}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```