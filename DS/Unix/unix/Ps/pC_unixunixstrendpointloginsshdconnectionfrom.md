#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-sshdconnectionfrom"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
    """sshd["""
    """ Connection from """
  ]
  Fields = [
    """({host}\S+) sshd\["""
    """\ssshd\[\d+\]:\s*({additional_info}.+?)\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```