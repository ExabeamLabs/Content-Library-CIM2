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
    """\s({time}\d{10})\.\d+\s""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """Original Address=({host}[^\s]+)\s""",
    """authentication on ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """for user ({user}[\w\.\-]{1,40}\$?)\s""",
    """as ({user_ou}.*) with""",
    """policy for group ({group_name}.+?)\s*$""",
  ]


}
```