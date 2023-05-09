#### Parser Content
```Java
{
Name = juniper-srx-str-app-logout-success-logout
  Vendor = Juniper Networks
  Product = Juniper SRX Series
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """NetScreen""", """ device_id=""", """has logged out""" ]
  Fields = [
    """\Wdevice_id=({host}[\w\-.]+)\s+""",# severity_level is removed
    """\(({time}\d\d\d\d-\d\d-\d\d \d\d\:\d\d:\d\d)\)""",
    """\s+({user}\S+)\s+has logged out.+?from ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```