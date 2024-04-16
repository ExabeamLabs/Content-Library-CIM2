#### Parser Content
```Java
{
Name = "cisco-ise-kv-app-activity-success-cisesystemstatistics"
Vendor = "Cisco"
Product = "Cisco ISE"
TimeFormat = ["yyyy-MM-dd HH:mm:ss.SSS z", "MMM dd HH:mm:ss"]
ParserVersion = "v1.0.0"
Conditions = [ """ CISE_System_Statistics """ ]
Fields = [
  """({time}\w{3}\s+\d{1,2}\s(\d\d\d\d\s)?\d\d:\d\d:\d\d)\s+"""
  """\w\w\w\s*\d+\s*\d\d:\d\d:\d\d ({host}[\w\-\.]+)\s({event_name}CISE_System_Statistics)\s+\d+\s*\d+\s*\d+\s*({additional_info}({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d.\d\d\d (\+|\-)\d\d:\d\d)?[^$]+)\s*($)"""
        ]


}
```