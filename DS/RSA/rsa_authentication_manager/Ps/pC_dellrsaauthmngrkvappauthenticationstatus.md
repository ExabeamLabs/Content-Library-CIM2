#### Parser Content
```Java
{
Name = dell-rsaauthmngr-kv-app-authentication-status
  Vendor = RSA
  Product = RSA Authentication Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """SINGLEPOINT@34162""", """SYSTEM_""", """STATUS""" ]
  Fields = [
    """({host}[\w\-.]+) \d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))\sSINGLEPOINT.+({event_name}SYSTEM_.+STATUS)\s({additional_info}\[.+)\.""",
  ]
  ParserVersion = "v1.0.0"


}
```