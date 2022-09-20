#### Parser Content
```Java
{
Name = cisco-fp-kv-app-authentication-success-original
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """Original Address=""", """authentication on""" ]
  Fields = [
    """\s({time}\d+)\.\d+\s""",
    """Original Address=({host}[^\s]+)\s""",
    """authentication on ({dest_ip}\d+.\d+.\d+.\d+)""",
    """for user ({user}[^\s]+)\s""",
    """as ({user_ou}.*) with""",
    """policy for group ({group_name}.+?)\s*$""",
  ]


}
```