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
    """({event_name}({result}error) retrieving information about user (({domain}[^\s\\]+)\\)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  ParserVersion = "v1.0.0"


}
```