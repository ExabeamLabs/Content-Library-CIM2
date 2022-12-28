#### Parser Content
```Java
{
Name = juniper-srx-str-app-activity-netscreen
  ParserVersion = "v1.0.0"
  Vendor = Juniper Networks
  Product = Juniper SRX Series
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """NetScreen""", """ device_id=""" ]
  Fields = [
    """\Wdevice_id=({device_id}[\w\-.]+)\s+""",# severity_level is removed
    """\(({time}\d\d\d\d-\d\d-\d\d \d\d\:\d\d:\d\d)\)""",
    """\[[^\[\]]*\][^:]+:\s+({additional_info}.+?)\s+\("""
  ]


}
```