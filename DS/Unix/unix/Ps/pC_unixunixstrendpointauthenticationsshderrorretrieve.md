#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-authentication-sshderrorretrieve"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
    """sshd["""
    """error retrieving information about user""" 
  ]
  Fields = [
    """(::ffff:)?({host}\S+) sshd\["""
    """({event_name}({result}error) retrieving information about user (({domain}[^\s\\]+)\\)?({user}\S+))"""
  ]
  ParserVersion = "v1.0.0"


}
```