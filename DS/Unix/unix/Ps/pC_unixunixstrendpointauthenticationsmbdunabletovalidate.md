#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-authentication-smbdunabletovalidate"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ 
  """smbd["""
  """unable to validate password for user"""
  ]
  Fields = [
    """({host}[\w.\-]+)\s+smbd\["""
    """\ssmbd\[\d+\]:\s*({event_name}.+?)\s*$"""
    """\suser ({user}.+?) in domain ({domain}.+?) to Domain controller"""
    """\sError was ({failure_reason}\w+)"""
  ]
  ParserVersion = "v1.0.0"


}
```