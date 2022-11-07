#### Parser Content
```Java
{
Name = juniper-srx-str-app-logout-success-logout
  Vendor = Juniper Networks
  Product = Juniper SRX
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """NetScreen""", """ device_id=""", """has logged out""" ]
  Fields = [
    """\Wdevice_id=({host}[\w\-.]+)\s+""",# severity_level is removed
    """\(({time}\d\d\d\d-\d\d-\d\d \d\d\:\d\d:\d\d)\)""",
    """\s+({user}\S+)\s+has logged out.+?from ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({src_port}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```