#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-authentication-sshdnotreceiveid"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
    """sshd["""
    """Did not receive identification string from"""
  ]
  Fields = [
    """({host}[\w.\-]+):? sshd\["""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
    """({failure_reason}({event_name}Did not receive identification string) from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  ]
  ParserVersion = "v1.0.0"


}
```