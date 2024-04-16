#### Parser Content
```Java
{
Name = zeek-z-str-app-activity-success-hosts
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """/known_hosts.log""" ]
  Fields = [
    """({time}\d{10})\.\d{6}\s+({host}[\w\-\.]+)\s*"""
    ]
  ParserVersion = "v1.0.0"


}
```