#### Parser Content
```Java
{
Name = juniper-srx-str-app-authentication-success-authsuccessfor
  Vendor = Juniper Networks
  Product = Juniper SRX
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """NetScreen""", """ device_id=""", """authentication successful for""" ]
  Fields = [
    """\Wdevice_id=({host}[\w\-.]+)\s+""",# severity_level is removed
    """\(({time}\d\d\d\d-\d\d-\d\d \d\d\:\d\d:\d\d)\)""",
    """authentication successful for (admin user|login name)\s+'?({user}[^'\s]+)'?""",
    """authentication successful for.+?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  ]
  ParserVersion = "v1.0.0"


}
```