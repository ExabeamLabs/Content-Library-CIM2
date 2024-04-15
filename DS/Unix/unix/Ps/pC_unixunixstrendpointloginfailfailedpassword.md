#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-fail-failedpassword"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """sshd["""
    """]: Failed password for """
  ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+"""
    """Message forwarded from ({host}[^\s:]+)"""
    """({event_code}ssh)"""
    """Failed password for (({email_address}[^@\s]+@[^\.\s]+\.[^\s]+)|({user}[^\s]+)) from (::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """ port ({src_port}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```