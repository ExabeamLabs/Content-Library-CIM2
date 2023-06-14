#### Parser Content
```Java
{
Name = pan-ngfw-csv-endpoint-login-success-system
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """,SYSTEM,""" , """,User""" ,  """ logged in """ ]
  Fields = [
    """SYSTEM,.+?({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
    """User ({user}.+?) logged in .+?from (({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^,]+))""",
    """,SYSTEM,([^,]*,){18}({host}[^\s,]+)""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```