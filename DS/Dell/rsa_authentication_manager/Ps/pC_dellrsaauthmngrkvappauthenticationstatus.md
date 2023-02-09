#### Parser Content
```Java
{
Name = dell-rsaauthmngr-kv-app-authentication-status
  Vendor = Dell
  Product = RSA Authentication Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """SINGLEPOINT@34162""", """SYSTEM_""", """STATUS""" ]
  Fields = [
    """({host}[\w\-.]+) \d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\sSINGLEPOINT.+({event_name}SYSTEM_.+STATUS)\s({additional_info}\[.+)\.""",
  ]
  ParserVersion = "v1.0.0"


}
```