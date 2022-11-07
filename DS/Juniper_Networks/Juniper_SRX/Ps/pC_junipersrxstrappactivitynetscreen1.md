#### Parser Content
```Java
{
Name = juniper-srx-str-app-activity-netscreen-1
  ParserVersion = "v1.0.0"
  Vendor = Juniper Networks
  Product = Juniper SRX
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """: NetScreen """, """ device_id=""", """ [Root]""" ]
  Fields = [
    """\sdevice_id=({host}.+?)\s+\[Root\]""",
    """\[Root\]\s*({event_name}[^:]+?)\-\d+:\s*({event_description}.+?)\.?\s*\(({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\)""",
  ]


}
```